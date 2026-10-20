<script setup lang="ts">
import GradientBackground from './GradientBackground.vue'
import StarField from './StarField.vue'
import SlideChrome from './SlideChrome.vue'
import { computed } from 'vue'
import { useNav, useSlideContext } from '@slidev/client'
import type { SlideFrameProps } from '../config/gradients'

withDefaults(defineProps<SlideFrameProps & { contentInset?: boolean }>(), {
  variant: 'right',
  showLogo: true,
  showNumbers: true,
  contentInset: false,
})

defineSlots<{
  default(): unknown
  background?(): unknown
  canvas?(): unknown
}>()

const { $renderContext } = useSlideContext()
const { isPrintMode } = useNav()
const sharedBackground = computed(() => !isPrintMode.value
  && ($renderContext.value === 'slide' || $renderContext.value === 'presenter'))
</script>

<template>
  <div class="slidev-layout slide-frame relative isolate w-full h-full p-0 overflow-hidden text-heading" :class="sharedBackground ? 'bg-transparent' : 'bg-canvas'">
    <GradientBackground v-if="!sharedBackground" :variant="variant" />
    <StarField v-if="!sharedBackground" />
    <div v-if="$slots.background" class="absolute inset-0 z-1 pointer-events-none"><slot name="background" /></div>
    <div class="slide-content absolute inset-x-gutter z-2" :class="contentInset ? 'top-[88px] bottom-[72px]' : 'inset-y-0'"><slot /></div>
    <div v-if="$slots.canvas" class="slide-canvas absolute inset-y-0 inset-x-gutter z-2"><slot name="canvas" /></div>
    <SlideChrome :show-logo="showLogo" :show-numbers="showNumbers" />
  </div>
</template>
