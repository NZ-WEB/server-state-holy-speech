<script setup lang="ts">
// The cache is revealed first; both consumers and their connectors follow together.
defineProps<{ stage: number }>()
</script>

<template>
  <div class="query-mutation-cache relative w-[1704px] h-[160px] font-body text-white" aria-live="polite">
    <div
      data-node="query-cache" data-stage="1"
      class="absolute top-0 left-[528px] box-border w-[648px] h-[160px] flex items-center justify-center p-[24px] rounded-[24px] border-2 border-solid border-accent bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="stage >= 1 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="stage < 1"
    >
      <p class="m-0 text-[40px] leading-[1.2] font-bold text-center">Query Cache</p>
    </div>

    <div
      data-stage="2"
      class="absolute inset-0 transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="stage >= 2 ? 'opacity-100' : 'opacity-0'"
      :aria-hidden="stage < 2"
    >
      <div data-node="use-query" data-stage="2" class="absolute top-0 left-0 box-border w-[402px] h-[160px] flex items-center justify-center p-[24px] rounded-[24px] border border-solid border-white/20 bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
        <p class="m-0 text-[32px] leading-[1.2] font-bold text-center">useQuery</p>
      </div>
      <div data-node="use-mutation" data-stage="2" class="absolute top-0 right-0 box-border w-[402px] h-[160px] flex items-center justify-center p-[24px] rounded-[24px] border border-solid border-white/20 bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
        <p class="m-0 text-[32px] leading-[1.2] font-bold text-center">useMutation</p>
      </div>
      <svg class="absolute inset-0 pointer-events-none overflow-visible" width="1704" height="160" viewBox="0 0 1704 160" aria-hidden="true">
        <g data-connection="use-query-cache" data-stage="2" stroke="#ed0f00" stroke-width="3" fill="#ed0f00">
          <path d="M402 80H516" fill="none" />
          <path d="M528 80L516 74V86Z" stroke="none" />
        </g>
        <g data-connection="use-mutation-cache" data-stage="2" stroke="#ed0f00" stroke-width="3" fill="#ed0f00">
          <path d="M1302 80H1188" fill="none" />
          <path d="M1176 80L1188 74V86Z" stroke="none" />
        </g>
      </svg>
    </div>
  </div>
</template>
