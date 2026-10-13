<script setup lang="ts">
import GradientBackground from './GradientBackground.vue'
import SlideChrome from './SlideChrome.vue'
import { computed } from 'vue'
import { useNav, useSlideContext } from '@slidev/client'
import type { SlideFrameProps } from '../config/gradients'

withDefaults(defineProps<SlideFrameProps>(), {
  variant: 'right',
  showLogo: true,
  showNumbers: true,
})

defineSlots<{
  default(): unknown
  background?(): unknown
}>()

const { $renderContext } = useSlideContext()
const { isPrintMode } = useNav()
const sharedBackground = computed(() => !isPrintMode.value
  && ($renderContext.value === 'slide' || $renderContext.value === 'presenter'))
</script>

<template>
  <div class="slidev-layout slide-frame relative isolate w-full h-full p-0 overflow-hidden text-heading" :class="sharedBackground ? 'bg-transparent' : 'bg-canvas'">
    <GradientBackground v-if="!sharedBackground" :variant="variant" />
    <div v-if="$slots.background" class="absolute inset-0 z-1 pointer-events-none"><slot name="background" /></div>
    <div class="relative z-2 h-full mx-gutter"><slot /></div>
    <SlideChrome :show-logo="showLogo" :show-numbers="showNumbers" />
  </div>
</template>
