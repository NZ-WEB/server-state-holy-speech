<script setup lang="ts">
const steps = [
  { title: 'Адрес', description: 'удалён', node: '1:1640', invalidation: false },
  { title: 'invalidate', description: 'списка адресов', node: '1:1646', invalidation: true },
  { title: 'refetch', description: 'адресов', node: '1:1652', invalidation: false },
  { title: 'Активный адрес', description: 'выбран заново', node: '1:1658', invalidation: false },
  { title: 'refetch', description: 'магазина', node: '1:1664', invalidation: false },
  { title: 'refetch', description: 'каталога', node: '1:1670', invalidation: false },
] as const
</script>

<template>
  <div class="refactor-invalidation-flow relative h-[648px] w-[836px] font-body font-bold leading-[1.2]">
    <div class="flex w-[744px] flex-col gap-[24px]">
      <div
        v-for="step in steps" :key="step.node" :data-node="step.node"
        class="box-border flex h-[88px] w-full shrink-0 flex-col items-center justify-center rounded-[24px] border-solid bg-white/5 px-[24px] py-[8px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
        :class="step.invalidation ? 'border-2 border-[#41e786]' : 'border border-white/20'"
      >
        <p class="m-0 w-full text-[32px] text-white">{{ step.title }}</p>
        <p class="m-0 w-full text-[24px] text-secondary">{{ step.description }}</p>
      </div>
    </div>
    <svg
      data-connection="invalidation-chain" class="pointer-events-none absolute top-0 left-[774px]"
      width="28" height="648" viewBox="0 0 28 648" fill="none" aria-hidden="true"
    >
      <path d="M14 2V630" stroke="#41e786" stroke-width="4" stroke-linecap="round" />
      <path d="M2 626L14 648L26 626H2Z" fill="#41e786" />
    </svg>
  </div>
</template>
