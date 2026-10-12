<script setup lang="ts">
import { computed } from 'vue'
import type { CSSProperties } from 'vue'
import { gradientVariants } from '../config/gradients'
import type { GradientSpot, GradientVariant } from '../config/gradients'

const props = withDefaults(defineProps<{ variant?: GradientVariant }>(), {
  variant: 'right',
})

const spots = computed(() => gradientVariants[props.variant] ?? gradientVariants.right)

function spotStyle(spot: GradientSpot): CSSProperties {
  const color = spot.color.join(', ')
  const stops = spot.stops.map(([position, alpha]) =>
    `rgba(${color}, ${alpha}) ${position}%`,
  ).join(', ')

  return {
    left: `${spot.x / 1920 * 100}%`,
    top: `${spot.y / 1080 * 100}%`,
    width: `${spot.width / 1920 * 100}%`,
    height: `${spot.height / 1080 * 100}%`,
    opacity: spot.opacity,
    background: `radial-gradient(ellipse closest-side, ${stops})`,
  }
}
</script>

<template>
  <div class="gradient-background absolute inset-0 overflow-hidden pointer-events-none" aria-hidden="true" :data-variant="variant">
    <div v-for="(spot, index) in spots" :key="index" class="gradient-spot absolute" :style="spotStyle(spot)" />
  </div>
</template>
