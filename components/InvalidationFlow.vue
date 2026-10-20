<script setup lang="ts">
defineProps<{ stage: number }>()
const steps = [
  { title: 'Action', description: 'данные изменились' },
  { title: 'Invalidate', description: 'кеш устарел' },
  { title: 'Refetch', description: 'новый запрос' },
  { title: 'Fresh cache', description: 'актуальная копия' },
] as const
</script>

<template>
  <div class="invalidation-flow flex h-[156px] w-[1760px] items-center justify-between" aria-live="polite">
    <template v-for="(step, index) in steps" :key="step.title">
      <div v-if="index > 0" class="invalidation-arrow relative h-0 w-[32px] shrink-0 transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= index + 1 ? 'opacity-100' : 'opacity-0'" aria-hidden="true">
        <PublicImage src="/images/invalidation-refresh-arrow.svg" alt="" width="34" height="14.7279" class="absolute left-[-1px] top-[-7.36395px] block max-w-none" />
      </div>
      <article class="invalidation-step relative box-border flex h-[156px] w-[402px] shrink-0 flex-col items-center justify-center gap-[4px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[24px] text-center font-body backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none" :class="stage >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'" :aria-hidden="stage < index + 1">
        <h2 class="m-0 w-full text-[30px] font-bold leading-[38px] text-white">{{ step.title }}</h2>
        <p class="m-0 w-full text-[24px] leading-[1.35] text-white/69">{{ step.description }}</p>
      </article>
    </template>
  </div>
</template>
