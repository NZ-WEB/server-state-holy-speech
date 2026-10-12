<script setup lang="ts">
import ImageSlide from '../components/ImageSlide.vue'
import type { SlideFrameProps } from '../config/gradients'

withDefaults(defineProps<SlideFrameProps & {
  image: string
  alt: string
  backgroundImage?: string
}>(), {
  variant: 'diagonal',
  showLogo: true,
  showNumbers: true,
})
</script>

<template>
  <ImageSlide :image="image" :alt="alt" :background-image="backgroundImage" :variant="variant" :show-logo="showLogo" :show-numbers="showNumbers">
    <slot />
  </ImageSlide>
</template>
