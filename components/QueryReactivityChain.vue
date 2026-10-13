<script setup lang="ts">
defineProps<{ stage: number }>()

const nodes = [
  { key: 'addresses-query', title: 'Addresses Query', description: 'список адресов', stage: 1, position: 'left-0', border: 'border border-white/20' },
  { key: 'active-address', title: 'Active Address', description: 'client store', stage: 2, position: 'left-[434px]', border: 'border border-white/20' },
  { key: 'store-query', title: 'Store Query', description: 'магазин по адресу', stage: 3, position: 'left-[868px]', border: 'border border-white/20' },
  { key: 'catalog-query', title: 'Catalog Query', description: 'каталог', stage: 4, position: 'left-[1302px]', border: 'border-2 border-[#41e786]' },
] as const
</script>

<template>
  <div class="query-reactivity-chain relative w-[1704px] h-[208px] font-body text-[32px] leading-[1.2]" aria-live="polite">
    <div
      v-for="node in nodes" :key="node.key" :data-node="node.key" :data-stage="node.stage"
      class="absolute top-0 box-border w-[402px] h-[208px] flex flex-col items-center justify-center gap-[16px] p-[24px] rounded-[24px] border-solid bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="[node.position, node.border, stage >= node.stage ? 'opacity-100' : 'opacity-0']"
      :aria-hidden="stage < node.stage"
    >
      <p class="m-0 w-full font-bold text-center text-white">{{ node.title }}</p>
      <p class="m-0 w-full font-normal text-center text-secondary">{{ node.description }}</p>
    </div>
    <svg class="absolute inset-0 pointer-events-none overflow-visible" width="1704" height="208" viewBox="108 592 1704 208" fill="none" aria-hidden="true">
      <g data-connection="addresses-to-active" data-stage="2" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= 2 ? 'opacity-100' : 'opacity-0'">
        <path d="M512 696H532" stroke="white" stroke-opacity="0.55" stroke-width="4" />
        <path d="M524 686L540 696L524 706V686Z" fill="white" fill-opacity="0.55" />
      </g>
      <g data-connection="active-to-store" data-stage="3" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= 3 ? 'opacity-100' : 'opacity-0'">
        <path d="M946 696H966" stroke="white" stroke-opacity="0.55" stroke-width="4" />
        <path d="M958 686L974 696L958 706V686Z" fill="white" fill-opacity="0.55" />
      </g>
      <g data-connection="store-to-catalog" data-stage="4" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= 4 ? 'opacity-100' : 'opacity-0'">
        <path d="M1380 696H1400" stroke="white" stroke-opacity="0.55" stroke-width="4" />
        <path d="M1392 686L1408 696L1392 706V686Z" fill="white" fill-opacity="0.55" />
      </g>
    </svg>
  </div>
</template>
