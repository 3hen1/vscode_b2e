<script setup lang="ts">
import { computed, ref, onMounted, onUnmounted } from 'vue'
import { handleBackground, resolveAssetUrl } from '../layoutHelper'

const props = defineProps({
  image: {
    type: String,
  },
  class: {
    type: String,
  },
  backgroundSize: {
    type: String,
    default: 'contain',
  },
})

const showModal = ref(false)
const imageScale = ref(1)
const imageTranslateX = ref(0)
const imageTranslateY = ref(0)
const isDragging = ref(false)
const lastMouseX = ref(0)
const lastMouseY = ref(0)

const imageUrl = computed(() => props.image ? resolveAssetUrl(props.image) : '')

const imageStyle = computed(() => ({
  transform: `scale(${imageScale.value}) translate(${imageTranslateX.value}px, ${imageTranslateY.value}px)`,
  transition: isDragging.value ? 'none' : 'transform 0.2s ease-out'
}))

const openImageModal = () => {
  showModal.value = true
  // Reset transform values
  imageScale.value = 1
  imageTranslateX.value = 0
  imageTranslateY.value = 0
}

const closeImageModal = () => {
  showModal.value = false
}

const handleWheel = (event: WheelEvent) => {
  if (!showModal.value) return
  
  event.preventDefault()
  const delta = event.deltaY > 0 ? 0.9 : 1.1
  const newScale = Math.max(0.5, Math.min(5, imageScale.value * delta))
  
  imageScale.value = newScale
  
  // Reset position if zoomed out too much
  if (newScale === 1) {
    imageTranslateX.value = 0
    imageTranslateY.value = 0
  }
}

const handleMouseDown = (event: MouseEvent) => {
  if (imageScale.value <= 1) return
  
  isDragging.value = true
  lastMouseX.value = event.clientX
  lastMouseY.value = event.clientY
}

const handleMouseMove = (event: MouseEvent) => {
  if (!isDragging.value || imageScale.value <= 1) return
  
  const deltaX = event.clientX - lastMouseX.value
  const deltaY = event.clientY - lastMouseY.value
  
  imageTranslateX.value += deltaX / imageScale.value
  imageTranslateY.value += deltaY / imageScale.value
  
  lastMouseX.value = event.clientX
  lastMouseY.value = event.clientY
}

const handleMouseUp = () => {
  isDragging.value = false
}

const handleKeydown = (event: KeyboardEvent) => {
  if (event.key === 'Escape') {
    closeImageModal()
  }
}

onMounted(() => {
  document.addEventListener('keydown', handleKeydown)
  document.addEventListener('wheel', handleWheel, { passive: false })
  document.addEventListener('mousemove', handleMouseMove)
  document.addEventListener('mouseup', handleMouseUp)
})

onUnmounted(() => {
  document.removeEventListener('keydown', handleKeydown)
  document.removeEventListener('wheel', handleWheel)
  document.removeEventListener('mousemove', handleMouseMove)
  document.removeEventListener('mouseup', handleMouseUp)
})
</script>

<template>
  <div class="flex w-full h-full">
    <div 
      class="flex-shrink-0 bg-center bg-no-repeat cursor-pointer relative overflow-hidden"
      :style="{ 
        backgroundImage: imageUrl ? `url(${imageUrl})` : 'none',
        backgroundSize: props.backgroundSize,
        width: 'auto',
        maxWidth: '40%',
        aspectRatio: '4/3'
      }"
      @click="openImageModal"
    >
      <div class="absolute inset-0 hover:bg-black hover:bg-opacity-10 transition-all duration-200 flex items-center justify-center">
        <div class="opacity-0 hover:opacity-100 transition-opacity duration-200 bg-black bg-opacity-50 text-white px-3 py-1 rounded text-sm">
          Click to view large image
        </div>
      </div>
    </div>
    <div class="flex-1 slidev-layout default overflow-y-auto ml-4" :class="props.class">
      <slot />
    </div>
    
    <!-- Modal for image popup -->
    <div 
      v-if="showModal" 
      class="fixed inset-0 bg-black bg-opacity-80 flex items-center justify-center z-50"
      @click="closeImageModal"
    >
      <div class="max-w-[90vw] max-h-[90vh] relative overflow-hidden">
        <img 
          :src="imageUrl" 
          alt="Large view"
          class="max-w-full max-h-full object-contain select-none"
          :style="imageStyle"
          @click.stop
          @mousedown="handleMouseDown"
          draggable="false"
        />
        <button 
          @click="closeImageModal"
          class="absolute top-4 right-4 text-white text-2xl bg-black bg-opacity-50 rounded-full w-10 h-10 flex items-center justify-center hover:bg-opacity-70 transition-all z-10"
        >
          ×
        </button>
        <!-- Zoom indicator -->
        <div class="absolute bottom-4 left-4 text-white text-sm bg-black bg-opacity-50 px-3 py-1 rounded">
          {{ Math.round(imageScale * 100) }}% | Scroll to zoom, drag to pan
        </div>
      </div>
    </div>
  </div>
</template>
