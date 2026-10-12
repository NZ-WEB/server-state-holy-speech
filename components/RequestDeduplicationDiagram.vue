<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $clicks } = useSlideContext()
const consumers = [
  { title: 'Каталог', description: 'нужен активный адрес', top: 'top-[324px]' },
  { title: 'Магазин', description: 'нужен активный адрес', top: 'top-[524px]' },
  { title: 'Список адресов', description: 'работает с\u00a0адресами', top: 'top-[724px]' },
] as const
const requests = [
  { image: '/images/dedup-request-catalog.svg', labelTop: 'top-[380px]' },
  { image: '/images/dedup-request-store.svg', labelTop: 'top-[560px]' },
  { image: '/images/dedup-request-list.svg', labelTop: 'top-[798px]' },
] as const
</script>

<template>
  <div class="request-deduplication-diagram relative h-full font-body" aria-live="polite">
    <div
      class="dedup-store absolute left-[896px] top-[496px] box-border flex h-[224px] w-[836px] flex-col items-center justify-center gap-[20px] rounded-[24px] border-2 border-solid border-accent bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= 1 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="$clicks < 1"
    >
      <p class="m-0 w-[788px] font-bold text-[40px] leading-[48px] text-white">useAddressesListStore</p>
      <p class="m-0 w-[788px] font-bold text-[24px] leading-[26.4px] text-muted">activeAddress</p>
    </div>

    <article
      v-for="consumer in consumers"
      :key="consumer.title"
      class="dedup-consumer absolute left-[28px] box-border flex h-[160px] w-[402px] flex-col items-center justify-center gap-[20px] rounded-[24px] border border-solid border-[rgba(16,16,16,0.1)] bg-white/5 px-[24px] text-center backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] before:content-[''] before:absolute before:inset-[-1px] before:rounded-[24px] before:pointer-events-none before:p-[1px] before:bg-[linear-gradient(135deg,rgba(255,255,255,0.32),rgba(255,255,255,0.24))] before:[mask:linear-gradient(#fff_0_0)_content-box,linear-gradient(#fff_0_0)] before:![mask-composite:exclude] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="[consumer.top, $clicks >= 2 ? 'opacity-100' : 'opacity-0']"
      :aria-hidden="$clicks < 2"
    >
      <p class="m-0 w-[354px] text-[32px] leading-[38.4px] text-white">{{ consumer.title }}</p>
      <p class="m-0 w-[354px] font-bold text-[24px] leading-[26.4px] text-muted">{{ consumer.description }}</p>
    </article>

    <div
      class="dedup-requests absolute inset-0 pointer-events-none transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= 3 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="$clicks < 3"
    >
      <template v-for="request in requests" :key="request.image">
        <img class="dedup-request-arrow absolute left-[430px] top-[324px] block max-w-none" :src="request.image" alt="" width="466" height="560" aria-hidden="true" />
        <p class="absolute left-[462px] m-0 w-[402px] text-center font-bold text-[24px] leading-[26.4px] text-accent" :class="request.labelTop">loadAddresses()</p>
      </template>
    </div>
  </div>
</template>
