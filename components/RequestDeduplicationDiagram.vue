<script setup lang="ts">
import { useSlideContext } from '@slidev/client'
const { $clicks } = useSlideContext()
const consumers = [
  { title: 'Каталог', description: 'нужен активный адрес', top: 'top-[210px]' },
  { title: 'Магазин', description: 'нужен активный адрес', top: 'top-[398px]' },
  { title: 'Список адресов', description: 'работает с\u00a0адресами', top: 'top-[586px]' },
] as const
const requests = [
  { image: '/images/dedup-refresh-catalog.svg', x: 402, y: 210, width: 466, height: 560 },
  { image: '/images/dedup-refresh-shop.svg', x: 410, y: 474.795, width: 442.75, height: 18.4099 },
  { image: '/images/dedup-refresh-addresses.svg', x: 410, y: 543.23, width: 443.252, height: 123.897 },
] as const
</script>

<template>
  <div class="request-deduplication-diagram relative h-full font-body" aria-live="polite">
    <div class="dedup-store absolute left-[868px] top-[378px] box-border flex h-[220px] w-[892px] flex-col items-center justify-center gap-[8px] rounded-[24px] border-2 border-solid border-white/20 bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="$clicks >= 1 ? 'opacity-100' : 'opacity-0'" :aria-hidden="$clicks < 1">
      <p class="m-0 w-[788px] font-bold text-[40px] leading-[48px] text-white">useAddressesListStore</p>
      <p class="m-0 w-[788px] text-[24px] leading-[1.35] text-muted">activeAddress</p>
    </div>
    <article v-for="consumer in consumers" :key="consumer.title" class="dedup-consumer absolute left-0 box-border flex h-[156px] w-[402px] flex-col items-center justify-center gap-[4px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="[consumer.top, $clicks >= 2 ? 'opacity-100' : 'opacity-0']" :aria-hidden="$clicks < 2">
      <p class="m-0 w-[354px] font-bold text-[30px] leading-[38px] text-white">{{ consumer.title }}</p>
      <p class="m-0 w-[354px] text-[24px] leading-[1.35] text-white/69">{{ consumer.description }}</p>
    </article>
    <div class="dedup-requests absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="$clicks >= 3 ? 'opacity-100' : 'opacity-0'" :aria-hidden="$clicks < 3">
      <PublicImage v-for="request in requests" :key="request.image" class="dedup-request-arrow absolute block max-w-none" :src="request.image" :style="{ left: `${request.x}px`, top: `${request.y}px` }" :width="request.width" :height="request.height" alt="" aria-hidden="true" />
      <p v-for="top in [266, 442, 666]" :key="top" class="absolute left-[410px] m-0 w-[448px] text-center font-bold text-[24px] leading-[26.4px] text-accent" :style="{ top: `${top}px` }">loadAddresses()</p>
    </div>
  </div>
</template>
