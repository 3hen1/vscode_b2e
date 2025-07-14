<template>
  <div class="ide-voting-container" p="1" bg="gradient-to-br from-slate-50 to-blue-50" rounded="lg" border="1 slate-200" shadow="md">
    <!-- Header Section -->
    <div class="header" text="center" mb="1" style="height: 33.47px; display: flex; flex-direction: column; justify-content: center;">
      <p class="subtitle" text="gray-600" style="font-size: 0.6rem; margin: 0; line-height: 1.2;">
        Choose your most used IDE and see real-time voting results
      </p>
      <div class="stats" flex="~ items-center justify-center gap-2" style="font-size: 0.55rem; margin: 2px 0 0 0;" text="gray-500">
        <span class="total-votes">Total Votes: {{ totalVotes }}</span>
        <span class="separator">•</span>
        <span class="participants">IDEs: {{ Object.keys(votes).filter(ide => votes[ide] > 0).length }}</span>
      </div>
    </div>

    <!-- Main Content Area: Two-column Layout -->
    <div class="main-content" grid="~ cols-1 lg:cols-2 gap-3">
      <!-- Left Column: Voting Buttons -->
      <div class="voting-section">
        <h5 class="section-title" style="font-size: 0.7rem;" font="semibold text-gray-700" mb="1">Choose Your IDE:</h5>
        <div class="voting-grid" grid="~ cols-3 gap-1.5">
          <button
            v-for="ide in ideList"
            :key="ide.name"
            @click="vote(ide.name)"
            class="vote-button"
            :class="{ 'voted': recentVotes.includes(ide.name) }"
            p="1.5"
            bg="white hover:blue-50 active:blue-100"
            border="1 transparent hover:blue-200 active:blue-300"
            rounded="md"
            transition="all duration-200"
            shadow="sm hover:md active:lg"
            transform="hover:scale-105 active:scale-95"
            text="center"
            :style="`--ide-color: ${ide.color}`"
          >
            <div class="button-content" flex="~ col items-center gap-0.25">
              <span class="ide-icon" style="font-size: 0.7rem;">{{ ide.icon }}</span>
              <span class="ide-name" style="font-size: 0.5rem;" font="medium text-gray-700">{{ ide.name }}</span>
              <span class="vote-count" style="font-size: 0.45rem;" text="gray-500" bg="gray-100" px="0.75" py="0.125" rounded="full">
                {{ votes[ide.name] || 0 }}
              </span>
            </div>
          </button>
        </div>
      </div>

      <!-- Right Column: Results Display -->
      <div class="results-section">
        <div class="section-header" flex="~ items-center justify-between" mb="1">
          <h5 class="section-title" style="font-size: 0.7rem;" font="semibold text-gray-700">Real-time Results</h5>
          <button
            @click="clearVotes"
            class="clear-button"
            bg="red-50 hover:red-100"
            style="font-size: 0.5rem;"
            font="medium text-red-600 hover:text-red-700"
            border="1 red-200 hover:red-300"
            px="1.5" py="0.25"
            rounded="sm"
            transition="all duration-200"
            transform="hover:scale-105"
          >
            🗑️ Clear
          </button>
        </div>

        <!-- Bar Chart -->
        <div class="chart-container" bg="white" p="1.5" rounded="md" border="1 slate-200" shadow="inner">
          <div class="chart" space="y-1">
            <div
              v-for="(ide, index) in sortedResults.slice(0, 8)"
              :key="ide.name"
              class="chart-bar"
              :class="{ 'highlight': ide.votes > 0 }"
            >
              <div class="bar-info" flex="~ items-center justify-between" mb="0.5">
                <div class="bar-label" flex="~ items-center gap-1">
                  <span class="rank" 
                    :class="index < 3 ? `rank-${index + 1}` : 'rank-other'"
                    w="3" h="3" rounded="full" flex="~ items-center justify-center" style="font-size: 0.5rem;" font="bold text-white"
                  >
                    {{ index + 1 }}
                  </span>
                  <span class="ide-icon" style="font-size: 0.6rem;">{{ getIdeIcon(ide.name) }}</span>
                  <span class="ide-name" font="medium text-gray-700" style="font-size: 0.6rem;">{{ ide.name }}</span>
                </div>
                <div class="bar-stats" flex="~ items-center gap-1" style="font-size: 0.55rem;">
                  <span class="vote-count" font="semibold text-gray-900">{{ ide.votes }}</span>
                  <span class="percentage" text="gray-500">({{ ide.percentage }}%)</span>
                </div>
              </div>
              <div class="bar-track" bg="gray-100" h="1.5" rounded="full" overflow="hidden">
                <div
                  class="bar-fill"
                  :style="`
                    width: ${ide.percentage}%; 
                    background: linear-gradient(90deg, ${getIdeColor(ide.name)}, ${getIdeColor(ide.name)}dd);
                    transition: width 0.8s cubic-bezier(0.4, 0, 0.2, 1);
                  `"
                  h="full"
                  rounded="full"
                  shadow="sm"
                ></div>
              </div>
            </div>
          </div>

          <div v-if="totalVotes === 0" class="empty-state" text="center" py="2">
            <div class="empty-icon" style="font-size: 1.25rem;" mb="0.5" opacity="50">📊</div>
            <p class="empty-text" text="gray-500" style="font-size: 0.55rem;">No votes yet, cast the first vote!</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Vote Animation Effects -->
    <div
      v-for="animation in voteAnimations"
      :key="animation.id"
      class="vote-animation"
      :style="`
        position: fixed;
        left: ${animation.x}px;
        top: ${animation.y}px;
        z-index: 1000;
        pointer-events: none;
        animation: voteFloat 1.5s ease-out forwards;
      `"
    >
      <div class="animation-content" style="font-size: 1rem;" transform="scale-100">
        {{ animation.icon }} +1
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, computed, reactive } from 'vue'

// IDE列表配置
const ideList = [
  { name: 'VS Code', icon: '🔷', color: '#007ACC' },
  { name: 'IntelliJ IDEA', icon: '🧠', color: '#FF6B35' },
  { name: 'NeoVim', icon: '⚡', color: '#57A143' },
  { name: 'Android Studio', icon: '🤖', color: '#3DDC84' },
  { name: 'PyCharm', icon: '🐍', color: '#21D789' },
  { name: 'Jupyter Notebook', icon: '📓', color: '#F37626' },
  { name: 'Sublime', icon: '🎨', color: '#FF9800' },
  { name: 'Eclipse', icon: '🌙', color: '#2C2255' },
  { name: 'Xcode', icon: '🍎', color: '#1575F9' },
  { name: 'WebStorm', icon: '🌊', color: '#07C3F2' },
  { name: 'GoLand', icon: '🐹', color: '#00ADD8' },
  { name: 'Emacs', icon: '⌨️', color: '#7F5AB6' },
  { name: 'Cursor', icon: '👆', color: '#000000' },
  { name: 'Windsurf', icon: '🏄', color: '#00D4FF' },
  { name: 'Claude Code', icon: '🤖', color: '#FF6B35' },
  { name: 'Gemini CLI', icon: '💎', color: '#4285F4' },
  { name: 'Trae', icon: '🔀', color: '#6366F1' },
]

// 投票数据
const votes = reactive<Record<string, number>>({})

// 最近投票记录（用于动画效果）
const recentVotes = ref<string[]>([])

// 投票动画数组
const voteAnimations = ref<Array<{
  id: number
  x: number
  y: number
  icon: string
}>>([])

// 初始化投票数据
ideList.forEach(ide => {
  if (!(ide.name in votes)) {
    votes[ide.name] = 0
  }
})

// 计算总投票数
const totalVotes = computed(() => {
  return Object.values(votes).reduce((sum, count) => sum + count, 0)
})

// 计算排序后的结果
const sortedResults = computed(() => {
  return ideList
    .map(ide => ({
      name: ide.name,
      votes: votes[ide.name] || 0,
      percentage: totalVotes.value > 0 ? Math.round((votes[ide.name] || 0) / totalVotes.value * 100) : 0
    }))
    .sort((a, b) => b.votes - a.votes)
})

// 获取IDE图标
const getIdeIcon = (ideName: string) => {
  const ide = ideList.find(i => i.name === ideName)
  return ide?.icon || '💻'
}

// 获取IDE颜色
const getIdeColor = (ideName: string) => {
  const ide = ideList.find(i => i.name === ideName)
  return ide?.color || '#6366F1'
}

// 投票函数
const vote = (ideName: string) => {
  votes[ideName] = (votes[ideName] || 0) + 1
  
  // 添加到最近投票记录
  recentVotes.value.push(ideName)
  setTimeout(() => {
    const index = recentVotes.value.indexOf(ideName)
    if (index > -1) {
      recentVotes.value.splice(index, 1)
    }
  }, 500)

  // 创建投票动画
  createVoteAnimation(ideName)
}

// 创建投票动画
const createVoteAnimation = (ideName: string) => {
  const icon = getIdeIcon(ideName)
  const id = Date.now() + Math.random()
  
  // 获取随机位置
  const x = Math.random() * (window.innerWidth - 100) + 50
  const y = Math.random() * (window.innerHeight - 100) + 50
  
  voteAnimations.value.push({ id, x, y, icon })
  
  // 1.5秒后移除动画
  setTimeout(() => {
    const index = voteAnimations.value.findIndex(anim => anim.id === id)
    if (index > -1) {
      voteAnimations.value.splice(index, 1)
    }
  }, 1500)
}

// Clear votes
const clearVotes = () => {
  if (confirm('Are you sure you want to clear all voting data?')) {
    Object.keys(votes).forEach(key => {
      votes[key] = 0
    })
    recentVotes.value = []
    voteAnimations.value = []
  }
}
</script>

<style scoped>
.ide-voting-container {
  max-width: 800px;
  margin: 0 auto;
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
}

.vote-button {
  position: relative;
  overflow: hidden;
}

.vote-button.voted {
  background: linear-gradient(135deg, var(--ide-color, #6366F1) 0%, var(--ide-color, #6366F1)dd 100%);
  color: white;
  border-color: var(--ide-color, #6366F1);
  transform: scale(1.05);
}

.vote-button.voted .ide-name {
  color: white;
}

.vote-button.voted .vote-count {
  background: rgba(255, 255, 255, 0.2);
  color: white;
}

.vote-button::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.3), transparent);
  transform: translateX(-100%) translateY(-100%) rotate(45deg);
  transition: transform 0.6s;
}

.vote-button:hover::before {
  transform: translateX(100%) translateY(100%) rotate(45deg);
}

.rank-1 { background: linear-gradient(135deg, #FFD700, #FFA500); }
.rank-2 { background: linear-gradient(135deg, #C0C0C0, #A0A0A0); }
.rank-3 { background: linear-gradient(135deg, #CD7F32, #A0522D); }
.rank-other { background: linear-gradient(135deg, #6B7280, #4B5563); }

.chart-bar.highlight {
  transform: scale(1.01);
  transition: transform 0.3s ease;
}

.chart-bar:hover {
  background: rgba(59, 130, 246, 0.05);
  border-radius: 0.5rem;
  padding: 0.25rem;
  margin: -0.25rem;
}

@keyframes voteFloat {
  0% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
  50% {
    opacity: 1;
    transform: translateY(-30px) scale(1.1);
  }
  100% {
    opacity: 0;
    transform: translateY(-60px) scale(0.9);
  }
}

.empty-state {
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 0.5; }
  50% { opacity: 0.8; }
}

/* Responsive Design */
@media (max-width: 1024px) {
  .main-content {
    grid-template-columns: 1fr;
  }
  
  .voting-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}

@media (max-width: 768px) {
  .voting-grid {
    grid-template-columns: repeat(3, 1fr);
  }
  
  .ide-voting-container {
    padding: 0.25rem;
  }
  
  .title {
    font-size: 0.875rem;
  }
}

@media (max-width: 480px) {
  .voting-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .bar-info {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.125rem;
  }
  
  .bar-stats {
    align-self: flex-end;
  }
}
</style>
