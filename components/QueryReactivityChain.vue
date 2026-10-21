<script setup lang="ts">
defineProps<{ stage: number }>()

const nodes = [
  { key: 'addresses-query', title: 'Addresses Query', description: 'список адресов', stage: 1 },
  { key: 'active-address', title: 'Active Address', description: 'client store', stage: 2 },
  { key: 'store-query', title: 'Store Query', description: 'магазин по адресу', stage: 3 },
  { key: 'catalog-query', title: 'Catalog Query', description: 'каталог', stage: 4 },
] as const

const arrow = `${import.meta.env.BASE_URL}images/figma-query-reactivity-arrow.svg`
</script>

<template>
  <div class="query-reactivity-chain relative flex w-[1760px] h-[156px] items-center justify-between font-body" aria-live="polite">
    <template v-for="(node, index) in nodes" :key="node.key">
      <div
        :data-node="node.key" :data-stage="node.stage"
        class="reactivity-glass-card relative box-border w-[402px] h-[156px] shrink-0 flex flex-col items-center justify-center gap-[4px] px-[24px] py-[40px] rounded-[24px] border border-solid bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
        :class="[index === 0 ? 'border-white/20' : 'border-[rgba(16,16,16,0.1)]', stage >= node.stage ? 'opacity-100' : 'opacity-0']"
        :aria-hidden="stage < node.stage"
      >
        <p class="m-0 w-full font-bold text-[30px] leading-[38px] text-center text-white">{{ node.title }}</p>
        <p class="m-0 w-full font-normal text-[24px] leading-[1.35] text-center text-[rgba(255,255,255,0.69)]">{{ node.description }}</p>
      </div>
      <div
        v-if="index < nodes.length - 1"
        :data-connection="`${node.key}-to-${nodes[index + 1].key}`" :data-stage="node.stage + 1"
        class="relative h-0 w-[32px] shrink-0 transition-opacity duration-500 ease-out motion-reduce:duration-0"
        :class="stage >= node.stage + 1 ? 'opacity-100' : 'opacity-0'"
        aria-hidden="true"
      >
        <img :src="arrow" alt="" width="34" height="14.7279" class="absolute left-[-1px] top-[-7.36395px] block max-w-none" />
      </div>
    </template>
  </div>
</template>

<style scoped>
.reactivity-glass-card::after {
  content: '';
  position: absolute;
  inset: -1px;
  border-radius: inherit;
  padding: 1px;
  background: linear-gradient(135deg, rgb(255 255 255 / 32%), rgb(255 255 255 / 10%) 36%, rgb(255 255 255 / 2%) 70%);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
  pointer-events: none;
}
</style>
