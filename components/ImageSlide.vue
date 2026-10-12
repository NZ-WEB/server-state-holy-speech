<script setup lang="ts">
import { computed, shallowRef } from 'vue'
import SlideFrame from './SlideFrame.vue'
import type { SlideFrameProps } from '../config/gradients'
import { assetUrl } from '../utils/asset-url'

const props = withDefaults(defineProps<SlideFrameProps & {
  image: string
  alt: string
  backgroundImage?: string
}>(), {
  variant: 'diagonal',
  showLogo: true,
  showNumbers: true,
})

const imageUrl = computed(() => assetUrl(props.image))
const backgroundUrl = computed(() => assetUrl(props.backgroundImage || props.image))
const imageRatio = shallowRef(1)

function measureImage(event: Event) {
  const image = event.target as HTMLImageElement
  imageRatio.value = image.naturalWidth / image.naturalHeight
}
</script>

<template>
  <SlideFrame :variant="variant" :show-logo="showLogo" :show-numbers="showNumbers">
    <template #background>
      <div class="absolute left-[-25%] top-[-53.7963%] w-[158.90625%] h-[161.01852%] blur-[125px]" aria-hidden="true">
        <PublicImage class="block w-full h-full max-w-none object-cover object-bottom rounded-[24px]" :src="backgroundUrl" alt="" />
        <div class="absolute inset-0 bg-[rgba(17,17,17,0.35)] rounded-[24px]" />
      </div>
    </template>
    <div class="grid place-items-center h-full">
      <figure class="relative w-[min(1389.61px,calc(792px*var(--image-ratio)),100%)] aspect-[var(--image-ratio)] m-0 rounded-[32px] overflow-hidden" :style="{ '--image-ratio': imageRatio }">
        <PublicImage class="block w-full h-full max-w-none object-contain" :src="imageUrl" :alt="alt" @load="measureImage" />
        <div v-if="$slots.default" class="absolute inset-0"><slot /></div>
      </figure>
    </div>
  </SlideFrame>
</template>
