<script setup lang="ts">
import SlideFrame from '../components/SlideFrame.vue'
import type { SlideFrameProps } from '../config/gradients'

withDefaults(defineProps<SlideFrameProps>(), {
  variant: 'right',
  showLogo: true,
  showNumbers: true,
})
</script>

<template>
  <SlideFrame :variant="variant" :show-logo="showLogo" :show-numbers="showNumbers">
    <slot />
  </SlideFrame>
</template>
