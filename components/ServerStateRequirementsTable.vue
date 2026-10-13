<script setup lang="ts">
defineProps<{ stage: number }>()

const rows = [
  { title: 'Queries / mutations', description: 'разделение ответственности' },
  { title: 'Query key', description: 'предсказуемая адресация данных' },
  { title: 'Дедупликация', description: 'один запрос для нескольких потребителей' },
  { title: 'Управление кэшем', description: 'прозрачное состояние данных' },
  { title: 'Реактивная модель данных', description: 'обновления без ручной синхронизации' },
] as const
</script>

<template>
  <div class="server-state-requirements-table flex w-[1704px] flex-col font-body text-[32px] leading-[1.2]" role="table" :data-stage="stage" aria-live="polite">
    <div
      v-for="(row, index) in rows"
      :key="row.title"
      class="box-border flex h-[112px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="stage >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :data-row="index + 1"
      :data-stage="index + 1"
      :aria-hidden="stage < index + 1"
      role="row"
    >
      <p class="m-0 w-[836px] shrink-0 font-bold text-white" role="cell">{{ row.title }}</p>
      <p class="m-0 w-[836px] shrink-0 font-normal text-secondary" role="cell">{{ row.description }}</p>
    </div>
  </div>
</template>
