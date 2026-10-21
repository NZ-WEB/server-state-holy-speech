<script setup lang="ts">
defineProps<{ stage: number }>()

// Coordinates are relative to the diagram's Figma origin (80, 298).
// Keep this order: later circles overlap earlier circles in the source frame.
const circles = [
  { node: '89:3453', x: 0, y: 0, title: 'Queries / mutations', description: 'разделение\nответственности' },
  { node: '89:3458', x: 328, y: 219, title: 'Query key', description: 'предсказуемая\nадресация данных' },
  { node: '89:3459', x: 656, y: 0, title: 'Дедупликация', description: 'один запрос\nдля нескольких\nпотребителей' },
  { node: '89:3460', x: 984, y: 220, title: 'Управление кэшем', description: 'прозрачное\nсостояние данных' },
  { node: '89:3461', x: 1312, y: 0, title: 'Реактивная\nмодель данных', description: 'обновления без ручной\nсинхронизации' },
] as const
</script>

<template>
  <ol class="requirement-circles absolute left-0 top-[210px] m-0 h-[668px] w-[1760px] list-none p-0 font-body" :data-stage="stage" aria-live="polite">
    <li
      v-for="(circle, index) in circles"
      :key="circle.node"
      class="requirement-circle absolute h-[448px] w-[448px] rounded-full"
      :class="{ 'requirement-circle-visible': stage >= index + 1 }"
      :style="{ left: `${circle.x}px`, top: `${circle.y}px`, zIndex: index + 1 }"
      :data-node-id="circle.node"
      :data-circle="index + 1"
      :aria-hidden="stage < index + 1"
    >
      <PublicImage class="absolute left-0 top-0 max-w-none" src="/images/requirements-circle.svg" alt="" aria-hidden="true" />
      <div class="absolute left-[61px] top-1/2 flex w-[327px] -translate-y-1/2 flex-col items-center gap-[20px] text-center">
        <p class="m-0 w-full whitespace-pre-line font-bold text-[32px] leading-[1.1] text-white">{{ circle.title }}</p>
        <p class="m-0 w-full whitespace-pre-line font-normal text-[28px] leading-[1.2] text-white/69">{{ circle.description }}</p>
      </div>
    </li>
  </ol>
</template>

<style scoped>
.requirement-circle {
  opacity: 0;
  visibility: hidden;
  transform: translateY(12px);
  backdrop-filter: blur(19px);
  transition: opacity 500ms ease-out, transform 500ms ease-out;
  pointer-events: none;
}

.requirement-circle-visible {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  .requirement-circle {
    transition: none;
    transform: none;
  }
}
</style>
