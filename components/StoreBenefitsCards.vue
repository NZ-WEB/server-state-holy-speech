<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $clicks } = useSlideContext()
const benefits = [
  {
    title: 'Single Source of Truth',
    description: 'Есть единое место управления логикой',
    image: '/images/store-benefit-truth-v2.png',
    alphaBounds: [0, 7, 1222, 1254],
    color: 'text-[#ff7166]',
  },
  {
    title: 'Devtools',
    description: 'Состояние и действия удобно наблюдать',
    image: '/images/store-benefit-devtools-v2.png',
    alphaBounds: [0, 0, 1236, 1230],
    color: 'text-[#a7b9f4]',
  },
  {
    title: 'Предсказуемая модель',
    description: 'Изменения проходят через понятные actions',
    image: '/images/store-benefit-model-v2.png',
    alphaBounds: [25, 32, 1234, 1204],
    color: 'text-[#86caa9]',
  },
  {
    title: 'Тестируемость',
    description: 'Store живёт независимо от lifecycle компонента',
    image: '/images/store-benefit-testing-v2.png',
    alphaBounds: [0, 8, 1245, 1254],
    color: 'text-[#e4bd83]',
  },
] as const

// Normalize the visible silhouette, not the PNG box: our regenerated sources have
// different transparent margins. Fit and center each silhouette in a 144px square.
const iconSlot = 160
const iconSize = 144
const cards = benefits.map(benefit => {
  const [left, top, right, bottom] = benefit.alphaBounds
  const scale = iconSize / Math.max(right - left, bottom - top)
  return {
    ...benefit,
    imageStyle: {
      width: `${1254 * scale}px`,
      height: `${1254 * scale}px`,
      left: `${(iconSlot - (right - left) * scale) / 2 - left * scale}px`,
      top: `${(iconSlot - (bottom - top) * scale) / 2 - top * scale}px`,
    },
  }
})
</script>

<template>
  <div class="store-benefits-cards grid grid-cols-2 gap-[32px]" aria-live="polite">
    <article
      v-for="(benefit, index) in cards"
      :key="benefit.title"
      class="store-benefit-card relative box-border flex h-[226px] min-w-0 items-center gap-[48px] rounded-[32px] border border-solid border-white/20 p-[32px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] before:content-[''] before:absolute before:inset-[-1px] before:rounded-[32px] before:pointer-events-none before:p-[1px] before:bg-[linear-gradient(135deg,rgba(255,255,255,0.32),rgba(255,255,255,0.24))] before:[mask:linear-gradient(#fff_0_0)_content-box,linear-gradient(#fff_0_0)] before:![mask-composite:exclude] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="$clicks >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :aria-hidden="$clicks < index + 1"
    >
      <div class="relative h-[160px] w-[160px] shrink-0" aria-hidden="true">
        <PublicImage :src="benefit.image" alt="" class="absolute max-w-none object-contain" :style="benefit.imageStyle" width="1254" height="1254" />
      </div>
      <div class="store-benefit-copy relative z-1 flex min-w-0 flex-1 flex-col gap-[12px] font-body">
        <h2 class="m-0 text-[32px] font-bold leading-[1.1]" :class="benefit.color">{{ benefit.title }}</h2>
        <p class="m-0 text-[28px] font-normal leading-[1.4] text-white/69">{{ benefit.description }}</p>
      </div>
    </article>
  </div>
</template>
