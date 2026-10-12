<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

const props = defineProps<{
  localBullets: readonly string[]
  applicationBullets: readonly string[]
}>()

const { $clicks } = useSlideContext()
const cards = computed(() => [
  { title: 'Local State', click: 1, bullets: props.localBullets },
  { title: 'Application State', click: 2, bullets: props.applicationBullets },
])
</script>

<template>
  <div class="state-types-cards grid grid-cols-2 items-stretch gap-[32px]" aria-live="polite">
    <article
      v-for="card in cards"
      :key="card.title"
      class="state-types-card relative box-border flex min-h-[316px] min-w-0 flex-col gap-[48px] rounded-[32px] border border-solid border-white/20 bg-white/5 px-[40px] pt-[40px] pb-[48px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] before:content-[''] before:absolute before:inset-[-1px] before:rounded-[32px] before:pointer-events-none before:p-[1px] before:bg-[linear-gradient(135deg,rgba(255,255,255,0.32),rgba(255,255,255,0.24))] before:[mask:linear-gradient(#fff_0_0)_content-box,linear-gradient(#fff_0_0)] before:![mask-composite:exclude] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0"
      :class="$clicks >= card.click ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :aria-hidden="$clicks < card.click"
    >
      <h2 class="relative z-1 m-0 font-heading font-black text-[40px] leading-[1.2] text-accent">{{ card.title }}</h2>
      <div class="relative z-1 flex flex-col gap-[8px] font-body font-normal text-[28px] leading-[1.35] text-secondary">
        <p v-for="bullet in card.bullets" :key="bullet" class="m-0 whitespace-pre-wrap">{{ `✦  ${bullet}` }}</p>
      </div>
    </article>
  </div>
</template>
