<script setup lang="ts">
const states = [
  { title: 'Server State', descriptions: ['Список адресов', 'Магазин', 'Каталог'], color: '#ff7166', node: '90:3863' },
  { title: 'Application State', descriptions: ['Активный адрес'], color: '#41e786', node: '90:3869' },
  { title: 'Local State', descriptions: ['Флаги модалок', 'Состояние компонентов'], color: '#7f9fff', node: '90:3874' },
] as const
</script>

<template>
  <div data-node="90:3862" class="refactor-state-cards grid h-[270px] w-[1760px] grid-cols-3 gap-[32px]">
    <article
      v-for="state in states"
      :key="state.title"
      :data-node="state.node"
      class="refactor-state-card relative box-border flex min-w-0 flex-col gap-[32px] rounded-[32px] border border-solid border-white/20 bg-white/5 p-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
    >
      <h2 class="relative z-1 m-0 w-full shrink-0 font-heading font-black text-[32px] leading-[1.2]" :style="{ color: state.color }">{{ state.title }}</h2>
      <div class="relative z-1 flex w-full shrink-0 flex-col font-body text-[28px] font-normal leading-[1.4] text-[rgba(255,255,255,0.69)]">
        <p v-for="description in state.descriptions" :key="description" class="m-0 w-full">{{ description }}</p>
      </div>
    </article>
  </div>
</template>

<style scoped>
.refactor-state-card::after {
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
