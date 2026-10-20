<script setup lang="ts">
const props = defineProps<{ stage: number }>()
const visible = (step: number) => props.stage >= step ? 'opacity-100' : 'opacity-0'
const regions = [
  { title: 'Backend', stage: 1, position: 'left-0 w-[402px]', tint: 'bg-[rgba(167,185,244,0.05)] border-[#a7b9f4]' },
  { title: 'Frontend', stage: 2, position: 'left-[442px] w-[1318px]', tint: 'bg-[rgba(228,189,131,0.05)] border-[#e4bd83]' },
] as const
const nodes = [
  { key: 'addresses', stage: 3, title: 'Адреса', description: 'True State', position: 'left-[32px] top-[302px] h-[156px]' },
  { key: 'api', stage: 4, title: 'API', description: '', position: 'left-[32px] top-[576px] h-[160px]' },
  { key: 'list', stage: 5, title: 'Список адресов', description: 'Client State', position: 'left-[474px] top-[302px] h-[156px]' },
  { key: 'ui', stage: 6, title: 'UI-компонент', description: '', position: 'left-[1390px] top-[302px] h-[160px]' },
  { key: 'add', stage: 7, title: 'Добавить адрес', description: '', position: 'left-[932px] top-[576px] h-[160px]' },
] as const
// Original Figma vectors, revealed with the corresponding destination.
const connections = [
  { key: 'addresses-to-api', stage: 4, image: '4220', x: 241.795, y: 554, width: 19, height: 104 },
  { key: 'api-to-addresses', stage: 4, image: '4218', x: 301.795, y: 552.75, width: 19, height: 104 },
  { key: 'http-get', stage: 5, image: '4219', x: 447.073, y: 545.75, width: 110, height: 121 },
  { key: 'read', stage: 6, image: '4221', x: 899, y: 458.795, width: 565, height: 19 },
  { key: 'ui-to-add', stage: 7, image: '4222', x: 1355.75, y: 558, width: 286, height: 196 },
  { key: 'invalidate', stage: 7, image: '4223', x: 713.795, y: 552.25, width: 287, height: 183 },
  { key: 'http-post', stage: 7, image: '4224', x: 456.75, y: 744.295, width: 544, height: 19 },
] as const
const labels = [
  { title: 'HTTP GET', stage: 5, x: 478, y: 487, size: 'text-[22px]' },
  { title: 'Read', stage: 6, x: 1072, y: 342, size: 'text-[24px]' },
  { title: 'Invalidate', stage: 7, x: 698, y: 545, size: 'text-[24px]' },
  { title: 'HTTP POST', stage: 7, x: 573, y: 680, size: 'text-[22px]' },
] as const
</script>

<template>
  <div class="client-cache-diagram relative h-full font-body text-white" role="group" aria-label="Жизненный цикл: Backend, Frontend, True State, API, список адресов, UI и добавление адреса">
    <div v-for="region in regions" :key="region.title" :data-region="region.title.toLowerCase()" :data-stage="region.stage" :aria-hidden="stage < region.stage" class="absolute top-[202px] h-[566px] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="[region.position, visible(region.stage)]">
      <p class="m-0 text-[40px] font-bold leading-[48px]">{{ region.title }}</p>
      <div class="absolute top-[68px] box-border h-[498px] w-full rounded-[32px] border border-solid" :class="region.tint" aria-hidden="true" />
    </div>
    <article v-for="node in nodes" :key="node.key" :data-node="node.key" :data-stage="node.stage" :aria-hidden="stage < node.stage" class="absolute box-border flex w-[338px] flex-col items-center justify-center gap-[4px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="[node.position, visible(node.stage)]">
      <p class="m-0 w-full text-[30px] font-bold leading-[38px]">{{ node.title }}</p>
      <p v-if="node.description" class="m-0 w-full text-[24px] leading-[1.35] text-white/69">{{ node.description }}</p>
    </article>
    <PublicImage v-for="connection in connections" :key="connection.key" :data-connection="connection.key" :data-stage="connection.stage" :src="`/images/lifecycle-${connection.image}.svg`" alt="" aria-hidden="true" class="absolute pointer-events-none block max-w-none transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="visible(connection.stage)" :width="connection.width" :height="connection.height" :style="{ left: `${connection.x - 80}px`, top: `${connection.y - 88}px` }" />
    <p v-for="label in labels" :key="label.title" :data-connection-label="label.title" :aria-hidden="stage < label.stage" class="absolute m-0 font-bold leading-[1.1] text-white/69 transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="[label.size, visible(label.stage)]" :style="{ left: `${label.x}px`, top: `${label.y}px` }">{{ label.title }}</p>
  </div>
</template>
