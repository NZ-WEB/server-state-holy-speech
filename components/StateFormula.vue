<script setup lang="ts">
import { computed, onBeforeUnmount, onMounted, shallowRef } from 'vue'
import { useSlideContext } from '@slidev/client'

const { $clicks } = useSlideContext()
const stateText = shallowRef<HTMLSpanElement | null>(null)
const stateWidth = shallowRef(0)
const showState = computed(() => $clicks.value >= 3)
let observer: ResizeObserver | undefined

function measureState() {
  const width = stateText.value?.offsetWidth ?? 0
  if (width > 0) stateWidth.value = width
}

onMounted(async () => {
  if (stateText.value) {
    observer = new ResizeObserver(measureState)
    observer.observe(stateText.value)
  }
  await document.fonts.ready
  // offsetWidth is measured in canvas pixels, independent of Slidev's scale.
  measureState()
})

onBeforeUnmount(() => observer?.disconnect())
</script>

<template>
  <div class="inline-flex items-baseline font-body font-semibold text-[280px] leading-[316.278px] text-white whitespace-pre" aria-live="polite" aria-atomic="true">
    <span>UI</span>
    <span v-click="1" class="inline-block !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0" :class="$clicks >= 1 ? 'translate-y-0' : 'translate-y-[12px]'"> = </span>
    <span v-click="2" class="inline-flex items-baseline !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0" :class="$clicks >= 2 ? 'translate-y-0' : 'translate-y-[12px]'">
      <span>f(</span>
      <span v-click="3" class="inline-flex items-baseline overflow-hidden !transition-[width,opacity,transform] !duration-500 ease-out motion-reduce:!duration-0" :class="showState ? 'translate-y-0' : 'translate-y-[12px]'" :style="{ width: showState ? `${stateWidth}px` : '0px' }">
        <span ref="stateText" class="inline-block w-max shrink-0">state</span>
      </span>
      <span>)</span>
    </span>
  </div>
</template>
