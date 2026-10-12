<script setup lang="ts">
defineProps<{ stage: number }>()

const steps = [
  { title: 'Mutation', description: 'данные изменились' },
  { title: 'Invalidate', description: 'кэш устарел' },
  { title: 'Refetch', description: 'новый запрос' },
  { title: 'Fresh cache', description: 'актуальная копия' },
] as const

const arrow = `${import.meta.env.BASE_URL}images/invalidation-arrow.svg`
</script>

<template>
  <div class="invalidation-flow flex h-[208px] w-[1704px] items-center gap-[4px]" aria-live="polite">
    <template v-for="(step, index) in steps" :key="step.title">
      <div
        v-if="index > 0"
        class="invalidation-arrow relative h-0 w-[32px] shrink-0 transition-opacity duration-500 ease-out motion-reduce:duration-0"
        :class="stage >= index + 1 ? 'opacity-100' : 'opacity-0'"
        aria-hidden="true"
      >
        <PublicImage :src="arrow" alt="" width="35" height="22.0919" class="absolute left-[-1.5px] top-[-11.04595px] block max-w-none" />
      </div>
      <article
        class="invalidation-step relative box-border flex h-[208px] w-[396px] shrink-0 flex-col items-center justify-center gap-[16px] rounded-[24px] border-solid bg-white/5 p-[24px] text-center font-body leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
        :class="[
          index === 1 ? 'border-2 border-[#41e786]' : 'border border-white/20',
          stage >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]',
        ]"
        :aria-hidden="stage < index + 1"
      >
        <h2 class="m-0 w-[354px] shrink-0 font-bold text-[40px] text-white">{{ step.title }}</h2>
        <p class="m-0 w-[354px] shrink-0 font-normal text-[32px] text-secondary">{{ step.description }}</p>
      </article>
    </template>
  </div>
</template>
