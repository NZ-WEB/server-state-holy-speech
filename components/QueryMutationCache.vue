<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{ stage: number }>()

// One model changes the list and every diagram label in the same render.
const labels = computed(() => props.stage >= 1
  ? { cache: 'Server State', read: 'useQuery', write: 'useMutation', notes: ['useQuery — чтение Server State', 'useMutation — запись Server State'] }
  : { cache: 'Cache', read: 'Read', write: 'Write', notes: ['Чтение из кеша', 'Запись в кеш'] })
</script>

<template>
  <section class="query-mutation-cache relative h-[376px] w-[1760px] font-body text-white" :data-stage="stage" aria-live="polite">
    <div class="cache-diagram absolute top-0 left-[788px] h-[376px] w-[972px]">
      <div data-node="cache" class="cache-card absolute top-[97px] left-0"></div>
      <div data-node="read" class="cache-card absolute top-0 left-[570px]"></div>
      <div data-node="write" class="cache-card absolute top-[220px] left-[570px]"></div>

      <div class="absolute top-[78px] left-[410px] flex h-[87px] w-[152px] items-center justify-center" aria-hidden="true">
        <PublicImage class="block max-w-none shrink-0 rotate-[150.21deg]" src="/images/cache-read-arrow-figma.svg" alt="" width="177.137" height="14.7279" />
      </div>
      <div class="absolute top-[194px] left-[410px] flex h-[104px] w-[152px] items-center justify-center" aria-hidden="true">
        <PublicImage class="block max-w-none shrink-0 rotate-[-145.62deg]" src="/images/cache-write-arrow-figma.svg" alt="" width="186.174" height="14.7279" />
      </div>
    </div>

    <Transition name="cache-copy" mode="out-in">
      <div :key="labels.cache" class="absolute inset-0">
        <DeckStarList class="absolute top-0 left-0 w-[720px]" :items="labels.notes" />
        <p class="cache-label absolute top-[97px] left-[788px]">{{ labels.cache }}</p>
        <p class="cache-label absolute top-0 left-[1358px]">{{ labels.read }}</p>
        <p class="cache-label absolute top-[220px] left-[1358px]">{{ labels.write }}</p>
      </div>
    </Transition>
  </section>
</template>

<style scoped>
.cache-card {
  box-sizing: border-box;
  display: flex;
  width: 402px;
  height: 156px;
  align-items: center;
  justify-content: center;
  border: 1px solid rgb(16 16 16 / 10%);
  border-radius: 24px;
  padding: 40px 24px;
  background: rgb(255 255 255 / 5%);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
}
.cache-label { display: grid; place-items: center; margin: 0; width: 402px; height: 156px; text-align: center; font-size: 30px; line-height: 38px; font-weight: 700; }
.cache-copy-enter-active,
.cache-copy-leave-active {
  transition: opacity 260ms ease, transform 260ms ease;
}
.cache-copy-enter-from { opacity: 0; transform: translateY(12px); }
.cache-copy-leave-to { opacity: 0; transform: translateY(-12px); }
@media (prefers-reduced-motion: reduce) {
  .cache-copy-enter-active,
  .cache-copy-leave-active { transition: none; }
  .cache-copy-enter-from,
  .cache-copy-leave-to { transform: none; }
}
.cache-card::before {
  content: '';
  position: absolute;
  inset: -1px;
  padding: 1px;
  border-radius: inherit;
  background: linear-gradient(135deg, rgb(255 255 255 / 40%), rgb(255 255 255 / 8%));
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
  pointer-events: none;
}
</style>
