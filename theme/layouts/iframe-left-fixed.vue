<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{
  url: string
  scale?: number
  width: number
  height: number
}>()

const scaleInvertPercent = computed(() => `${(1 / (props.scale || 1)) * 100}%`)
</script>

<template>
  <div class="grid grid-cols-2 w-full h-full">
    <div relative :style="{ width: scaleInvertPercent, height: scaleInvertPercent }">
      <iframe
        id="frame"
        class="w-full h-full"
        :src="url"
        :style="{
          width: `${width}px`,
          height: `${height}px`,
          transform: `scale(${scale || 1})`,
          transformOrigin: 'top left'
        }"
      />
    </div>
    <div class="slidev-layout default" v-bind="$attrs">
      <slot />
    </div>
  </div>
</template>
