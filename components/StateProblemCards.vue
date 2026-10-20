<script setup lang="ts">
defineProps<{ stage: number }>()
const cards = [
  { number: '01', caption: 'Загружаем', title: 'Список адресов', border: 'border-[#ff7166]', color: 'text-accent', image: '/images/state-problem-address-list-2x.png', imageStyle: { left: '82px', top: '-65.198px', width: '322px', height: '253px' } },
  { number: '02', caption: 'Выбираем', title: 'Активный адрес', border: 'border-[#41e786]', color: 'text-[#41e786]', image: '/images/state-problem-active-address-2x.png', imageStyle: { left: '82.691px', top: '-65.198px', width: '322px', height: '252px' } },
  { number: '03', caption: 'Находим по адресу', title: 'Магазин', border: 'border-[#ff7166]', color: 'text-accent', image: '/images/state-problem-shop-2x.png', imageStyle: { left: '87px', top: '-65px', width: '319px', height: '232px' } },
  { number: '04', caption: 'Подгружаем по магазину', title: 'Каталог', border: 'border-[#ff7166]', color: 'text-accent', image: '/images/state-problem-catalog-2x.png', imageStyle: { left: '89px', top: '-65.661px', width: '318px', height: '219px' } },
] as const
</script>

<template>
  <div class="state-problem-cards absolute top-[260px] left-0 grid w-full grid-cols-4 gap-[32px] font-body" aria-live="polite">
    <article v-for="(card, index) in cards" :key="card.number" :data-stage="index + 1" :aria-hidden="stage < index + 1" class="state-problem-card relative box-border flex h-[366px] min-w-0 flex-col justify-between rounded-[32px] border border-solid bg-white/5 p-[32px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none" :class="[card.border, stage >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]']">
      <p class="m-0 font-heading font-black text-[32px] leading-[1.2]" :class="card.color">{{ card.number }}</p>
      <PublicImage class="absolute z-1 block max-w-none" :style="card.imageStyle" :src="card.image" :alt="card.title" />
      <div class="flex flex-col gap-[4px]">
        <p class="m-0 text-[24px] leading-[1.35] text-white/69">{{ card.caption }}</p>
        <h2 class="m-0 text-[32px] font-bold leading-[1.1] text-white">{{ card.title }}</h2>
      </div>
    </article>
  </div>
</template>
