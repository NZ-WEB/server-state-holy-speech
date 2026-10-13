<script setup lang="ts">
defineProps<{ stage: number }>()

const consumers = [
  { key: 'addresses-list', title: 'Addresses List', position: 'left-0' },
  { key: 'catalog', title: 'Catalog', position: 'right-0' },
] as const
</script>

<template>
  <div class="shared-query-cache-diagram relative w-[1704px] h-[616px] font-body text-white" aria-live="polite">
    <div
      data-node="query-cache" data-stage="1"
      class="absolute top-[268px] left-[434px] box-border w-[836px] h-[144px] flex flex-col items-center justify-center gap-[16px] p-[24px] rounded-[24px] border-2 border-solid border-[#41e786] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="stage >= 1 ? 'opacity-100' : 'opacity-0'" :aria-hidden="stage < 1"
    >
      <p class="m-0 w-full text-center font-bold text-[40px] leading-[1.2]">Query Cache</p>
      <p class="m-0 w-full text-center font-normal text-secondary text-[32px] leading-[1.2]">['addresses']</p>
    </div>

    <div
      data-stage="2" class="absolute inset-0 transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="stage >= 2 ? 'opacity-100' : 'opacity-0'" :aria-hidden="stage < 2"
    >
      <div data-node="api" data-stage="2" class="absolute top-[520px] left-[434px] box-border w-[836px] h-[96px] flex items-center justify-center p-[24px] rounded-[24px] border border-solid border-white/20 bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
        <p class="m-0 w-full text-center font-bold text-[40px] leading-[1.2]">API</p>
      </div>
      <p data-label="one-request" data-stage="2" class="absolute top-[448px] left-[892px] m-0 w-[378px] text-[32px] leading-[1.2] font-bold text-[#41e786]">один запрос</p>
      <svg class="absolute inset-0 pointer-events-none overflow-visible" width="1704" height="616" viewBox="108 304 1704 616" fill="none" aria-hidden="true">
        <g data-connection="cache-to-api" data-stage="2">
          <path d="M960 728V804" stroke="#41e786" stroke-width="4" />
          <path d="M948 798L960 820L972 798H948Z" fill="#41e786" />
        </g>
      </svg>
    </div>

    <div
      data-stage="3" class="absolute inset-0 transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="stage >= 3 ? 'opacity-100' : 'opacity-0'" :aria-hidden="stage < 3"
    >
      <div
        v-for="consumer in consumers" :key="consumer.key" :data-node="consumer.key" data-stage="3"
        class="absolute top-0 box-border w-[836px] h-[152px] flex flex-col items-center justify-center gap-[16px] p-[24px] rounded-[24px] border border-solid border-white/20 bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
        :class="consumer.position"
      >
        <p class="m-0 w-full text-center font-bold text-[40px] leading-[1.2]">{{ consumer.title }}</p>
        <p class="m-0 w-full text-center font-normal text-secondary text-[32px] leading-[1.2]">useQuery(addresses)</p>
      </div>
      <svg class="absolute inset-0 pointer-events-none overflow-visible" width="1704" height="616" viewBox="108 304 1704 616" fill="none" aria-hidden="true">
        <g data-connection="addresses-to-cache" data-stage="3">
          <path d="M526 464V496C526 509.333 534 516 550 516H908C924 516 932 522.667 932 536V552" stroke="#41e786" stroke-width="4" />
          <path d="M920 546L932 568L944 546H920Z" fill="#41e786" />
        </g>
        <g data-connection="catalog-to-cache" data-stage="3">
          <path d="M1394 464V496C1394 509.333 1386 516 1370 516H1012C996 516 988 522.667 988 536V552" stroke="#41e786" stroke-width="4" />
          <path d="M976 546L988 568L1000 546H976Z" fill="#41e786" />
        </g>
      </svg>
    </div>
  </div>
</template>
