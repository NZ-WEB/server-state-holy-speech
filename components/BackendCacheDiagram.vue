<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

// One shared stage controls each destination and its connector together.
const { $clicks } = useSlideContext()
const assetBase = `${import.meta.env.BASE_URL}images/`
const destinations = [
  { key: 'database', title: 'Database', description: 'Источник истины', stage: 2, position: 'right-0', border: 'border border-white/20' },
  { key: 'cache', title: 'Cache', description: 'Готовая копия', stage: 3, position: 'left-0', border: 'border-2 border-[#41e786]' },
] as const
</script>

<template>
  <div class="backend-cache-diagram relative w-[836px] h-[536px] font-body text-[32px] leading-[38.4px] text-white" aria-live="polite">
    <div
      data-part="backend"
      class="absolute top-0 inset-x-0 box-border h-[168px] rounded-[24px] border-2 border-solid border-accent bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] flex flex-col justify-center items-center gap-[16px] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= 1 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="$clicks < 1"
    >
      <p class="m-0 w-[788px] text-center font-bold">Backend Server</p>
      <p class="m-0 w-[788px] text-center font-normal text-secondary">Источник запросов</p>
    </div>

    <div
      v-for="destination in destinations"
      :key="destination.key"
      :data-part="destination.key"
      class="absolute top-[360px] box-border w-[402px] h-[176px] rounded-[24px] border-solid bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] flex flex-col justify-center items-center gap-[16px] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="[destination.position, destination.border, $clicks >= destination.stage ? 'opacity-100' : 'opacity-0']"
      :aria-hidden="$clicks < destination.stage"
    >
      <p class="m-0 w-[354px] text-center font-bold">{{ destination.title }}</p>
      <p class="m-0 w-[354px] text-center font-normal text-secondary">{{ destination.description }}</p>
    </div>

    <div
      data-part="database-connection"
      class="absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= 2 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="$clicks < 2"
    >
      <PublicImage :src="`${assetBase}backend-database-arrow.svg`" alt="" class="absolute top-[171px] left-[480.5px] block max-w-none" width="167.546" height="183" />
      <p class="absolute top-[264px] left-[641px] w-[276px] m-0 text-[24px] leading-[28.8px] font-bold">5 секунд</p>
    </div>

    <div
      data-part="cache-connection"
      class="absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= 3 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="$clicks < 3"
    >
      <div class="absolute top-[171px] left-[204px] w-[156px] h-[182px] scale-x-[-1]">
        <PublicImage :src="`${assetBase}backend-cache-arrow.svg`" alt="" class="absolute top-0 left-[-1.5px] block max-w-none" width="168.546" height="183.5" />
      </div>
      <p class="absolute top-[264px] left-0 w-[402px] m-0 text-[24px] leading-[28.8px] font-bold text-[#41e786]">50 миллисекунд</p>
    </div>
  </div>
</template>
