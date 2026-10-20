<script setup lang="ts">
import { useSlideContext } from '@slidev/client'
const { $clicks } = useSlideContext()
const destinations = [
  { key: 'database', title: 'Database', description: 'Источник истины', stage: 2, position: 'right-0' },
  { key: 'cache', title: 'Cache', description: 'Готовая копия', stage: 3, position: 'left-0' },
] as const
</script>

<template>
  <div class="backend-cache-diagram relative h-[590px] w-[836px] font-body text-white" aria-live="polite">
    <div data-part="backend" class="absolute top-0 inset-x-0 box-border flex h-[220px] flex-col items-center justify-center gap-[8px] rounded-[24px] border-2 border-solid border-white/20 bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="$clicks >= 1 ? 'opacity-100' : 'opacity-0'" :aria-hidden="$clicks < 1">
      <p class="m-0 w-full text-[40px] font-bold leading-[48px]">Backend Server</p>
      <p class="m-0 w-full text-[24px] leading-[1.35] text-muted">Источник запросов</p>
    </div>
    <div v-for="destination in destinations" :key="destination.key" :data-part="destination.key" class="absolute top-[434px] box-border flex h-[156px] w-[402px] flex-col items-center justify-center gap-[4px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="[destination.position, $clicks >= destination.stage ? 'opacity-100' : 'opacity-0']" :aria-hidden="$clicks < destination.stage">
      <p class="m-0 w-full text-[30px] font-bold leading-[38px]">{{ destination.title }}</p>
      <p class="m-0 w-full text-[24px] leading-[1.35] text-white/69">{{ destination.description }}</p>
    </div>
    <div data-part="database-connection" class="absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="$clicks >= 2 ? 'opacity-100' : 'opacity-0'" :aria-hidden="$clicks < 2">
      <PublicImage src="/images/backend-refresh-database-arrow.svg" alt="" class="absolute top-[228px] left-[478.75px] block max-w-none" width="165.455" height="197.25" />
      <p class="absolute top-[336px] left-[635px] m-0 text-[24px] font-bold leading-[1.1] text-accent">5 секунд</p>
    </div>
    <div data-part="cache-connection" class="absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="$clicks >= 3 ? 'opacity-100' : 'opacity-0'" :aria-hidden="$clicks < 3">
      <PublicImage src="/images/backend-refresh-cache-arrow.svg" alt="" class="absolute top-[228px] left-[191px] block max-w-none -scale-x-100" width="166.455" height="198.25" />
      <p class="absolute top-[336px] left-0 m-0 text-[24px] font-bold leading-[1.1] text-[#41e786]">50 миллисекунд</p>
    </div>
  </div>
</template>
