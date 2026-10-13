<script setup lang="ts">
defineProps<{ stage: number }>()

// Each row has a separate left-to-right explanation; the second starts at click 5.
const cards = [
  { node: '1:1682', stage: 1, row: 0, column: 0, title: 'UI-компонент', key: '', description: 'читает адреса', active: false },
  { node: '1:1688', stage: 2, row: 0, column: 1, title: 'Query', key: "['addresses']", description: 'есть подписчик', active: true },
  { node: '1:1694', stage: 3, row: 0, column: 2, title: 'invalidate', key: '', description: 'кэш устарел', active: false },
  { node: '1:1700', stage: 4, row: 0, column: 3, title: 'refetch', key: '', description: 'сразу', active: true },
  { node: '1:1703', stage: 5, row: 1, column: 0, title: 'Нет компонента', key: '', description: 'никто не\u00a0читает', active: false },
  { node: '1:1709', stage: 6, row: 1, column: 1, title: 'Query', key: "['catalog']", description: 'нет подписчиков', active: false },
  { node: '1:1715', stage: 7, row: 1, column: 2, title: 'invalidate', key: '', description: 'кэш устарел', active: false },
  { node: '1:1721', stage: 8, row: 1, column: 3, title: 'Ожидание', key: '', description: 'до нового подписчика', active: false },
] as const

const connections = [
  { node: '1:1685', stage: 2, row: 0, column: 0 },
  { node: '1:1691', stage: 3, row: 0, column: 1 },
  { node: '1:1697', stage: 4, row: 0, column: 2 },
  { node: '1:1706', stage: 6, row: 1, column: 0 },
  { node: '1:1712', stage: 7, row: 1, column: 1 },
  { node: '1:1718', stage: 8, row: 1, column: 2 },
] as const
</script>

<template>
  <div class="active-query-flow relative h-[476px] w-[1704px] font-body text-[32px] leading-[1.2]" :data-stage="stage">
    <article
      v-for="card in cards"
      :key="card.node"
      :data-node="card.node"
      :data-stage="card.stage"
      :data-row="card.row"
      :aria-hidden="stage < card.stage"
      :style="{ left: `${card.column * 434}px`, top: `${card.row * 276}px` }"
      class="active-query-card absolute box-border flex h-[200px] w-[402px] flex-col items-center justify-center gap-[16px] rounded-[24px] border-solid bg-white/5 p-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="[card.active ? 'border-2 border-[#41e786]' : 'border border-white/20', stage >= card.stage ? 'opacity-100' : 'opacity-0']"
    >
      <p class="m-0 w-[354px] shrink-0 font-bold text-white">{{ card.title }}<template v-if="card.key"><br>{{ card.key }}</template></p>
      <p class="m-0 w-[354px] shrink-0 font-normal text-secondary">{{ card.description }}</p>
    </article>

    <svg
      v-for="connection in connections"
      :key="connection.node"
      :data-node="connection.node"
      :data-connection="connection.node"
      :data-stage="connection.stage"
      :aria-hidden="stage < connection.stage"
      :style="{ left: `${402 + connection.column * 434}px`, top: `${connection.row * 276 + 92}px` }"
      :class="[connection.row === 0 ? 'text-[#41e786]' : 'text-white/55', stage >= connection.stage ? 'opacity-100' : 'opacity-0']"
      class="absolute pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0"
      width="32" height="16" viewBox="0 0 32 16"
    >
      <path d="M 2 8 H 21" fill="none" stroke="currentColor" stroke-width="3" />
      <path d="M 20 2 L 30 8 L 20 14 Z" fill="currentColor" />
    </svg>
  </div>
</template>
