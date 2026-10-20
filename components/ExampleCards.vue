<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $clicks } = useSlideContext()
const stages = [
  { click: 1, number: '01', caption: 'Загружаем', title: 'Список адресов' },
  { click: 2, number: '02', caption: 'Выбираем', title: 'Активный адрес' },
  { click: 3, number: '03', caption: 'Находим по адресу', title: 'Магазин' },
  { click: 4, number: '04', caption: 'Подгружаем по магазину', title: 'Каталог' },
] as const
</script>

<template>
  <div class="grid grid-cols-4 gap-[32px]" aria-live="polite">
    <article
      v-for="stage in stages"
      :key="stage.number"
      v-click="stage.click"
      class="example-card relative flex h-[366px] min-w-0 flex-col justify-between box-border rounded-[32px] border border-solid border-white/20 bg-white/5 p-[32px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0"
      :style="{ transform: $clicks >= stage.click ? 'translateY(0)' : 'translateY(12px)' }"
      :aria-hidden="$clicks < stage.click"
    >
      <p class="relative z-1 m-0 w-full font-heading font-black text-[32px] leading-[1.2] text-muted">{{ stage.number }}</p>
      <div class="relative z-1 flex w-full flex-col gap-[4px]">
        <p class="m-0 font-body font-normal text-[24px] leading-[1.35] text-[rgba(255,255,255,0.69)] whitespace-nowrap">{{ stage.caption }}</p>
        <h2 class="m-0 font-body font-bold text-[32px] leading-[1.1] text-white whitespace-nowrap">{{ stage.title }}</h2>
      </div>
    </article>
  </div>
</template>
