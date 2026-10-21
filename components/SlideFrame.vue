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

const { $renderContext, $frontmatter } = useSlideContext()
const { isPrintMode } = useNav()
const sharedBackground = computed(() => !isPrintMode.value
  && ($renderContext.value === 'slide' || $renderContext.value === 'presenter'))
// Use this frame's metadata, never the active slide's useNav frontmatter:
// overview/presenter/print can render ordinary and image slides together.
const showStars = computed(() => $frontmatter.showStars !== false
  && !String($frontmatter.layout ?? 'default').startsWith('image'))
</script>

<template>
  <div class="slidev-layout slide-frame relative isolate w-full h-full p-0 overflow-hidden text-heading" :class="sharedBackground ? 'bg-transparent' : 'bg-canvas'">
    <GradientBackground v-if="!sharedBackground" :variant="variant" />
    <div v-if="$slots.background" class="absolute inset-0 z-1 pointer-events-none"><slot name="background" /></div>
    <div class="slide-content absolute inset-x-gutter z-2" :class="contentInset ? 'top-[88px] bottom-[72px]' : 'inset-y-0'">
      <slot />
      <!-- Last background at z−1: above opaque slot backdrops at z−1,
           below all foreground. Compensate the content inset to canvas0,0. -->
      <div v-if="showStars" class="absolute left-[-80px] z-[-1] w-[1920px] h-[1080px] pointer-events-none" :class="contentInset ? 'top-[-88px]' : 'top-0'" data-deck-star-layer>
        <StarField :animated="sharedBackground" />
      </div>
    </div>
    <div v-if="$slots.canvas" class="slide-canvas absolute inset-y-0 inset-x-gutter z-2"><slot name="canvas" /></div>
    <SlideChrome :show-logo="showLogo" :show-numbers="showNumbers" />
  </div>
</template>
