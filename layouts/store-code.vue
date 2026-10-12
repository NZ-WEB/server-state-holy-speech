<script setup lang="ts">
import SlideFrame from '../components/SlideFrame.vue'
import type { SlideFrameProps } from '../config/gradients'

withDefaults(defineProps<SlideFrameProps>(), {
  variant: 'store-left',
  showLogo: true,
  showNumbers: true,
})
</script>

<template>
  <SlideFrame
    :variant="variant"
    :show-logo="showLogo"
    :show-numbers="showNumbers"
    class="[&_.slide-logo]:!left-[108px] [&_.slide-logo]:!bottom-[76px] [&_.slide-number]:!right-[108px] [&_.slide-number]:!bottom-[74px] [&_.slide-number]:!w-[36px] [&_.slide-number]:!px-0"
  >
    <slot />
  </SlideFrame>
</template>
