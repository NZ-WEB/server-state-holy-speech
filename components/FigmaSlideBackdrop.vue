<script setup lang="ts">
withDefaults(defineProps<{
  showSecondary?: boolean
  secondaryX?: number
  secondaryY?: number
  focalX?: number
  focalY?: number
  focalSrc?: string
  focalWidth?: number
  focalHeight?: number
}>(), {
  showSecondary: true,
  secondaryX: -650,
  secondaryY: -580,
  focalX: -540,
  focalY: 280,
  focalSrc: '/images/figma-deck-red-focal.svg',
  focalWidth: 1600,
  focalHeight: 1250,
})
</script>

<template>
  <div class="figma-slide-backdrop" aria-hidden="true">
    <PublicImage v-if="showSecondary" class="figma-secondary" src="/images/figma-deck-red-secondary.svg" alt="" :style="{ left: `${secondaryX}px`, top: `${secondaryY}px` }" width="1300" height="1000" />
    <PublicImage class="figma-focal" :src="focalSrc" alt="" :style="{ left: `${focalX}px`, top: `${focalY}px` }" :width="focalWidth" :height="focalHeight" />
  </div>
</template>

<style scoped>
.figma-slide-backdrop {
  position: absolute;
  z-index: -1;
  left: -80px;
  top: -88px;
  width: 1920px;
  height: 1080px;
  overflow: hidden;
  pointer-events: none;
  background: #101010;
}
.figma-secondary, .figma-focal { position: absolute; display: block; max-width: none; }
</style>
