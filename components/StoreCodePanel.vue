<script setup lang="ts">
import { computed } from 'vue'
import type { CSSProperties } from 'vue'

const props = withDefaults(defineProps<{
  fontSize?: number
  lineHeight?: number
}>(), { fontSize: 27, lineHeight: 28 })

const typography = computed<CSSProperties>(() => ({
  '--slidev-code-font-size': `${props.fontSize}px`,
  '--slidev-code-line-height': `${props.lineHeight}px`,
}))

// The layout owns the panel width, so changing a snippet only resizes its height.
// Keep the native movement/resize timing and shorten only the token leave phase.
</script>

<template>
  <div
    class="store-code-panel box-border w-full min-w-0 flex-[1_1_0px] self-start rounded-[32px] border border-solid border-[#ed0f00]/25 bg-white/5 p-[32px] backdrop-blur-[19px] [--slidev-code-font-family:'Roboto_Mono',monospace] [--slidev-code-padding:0px] [--slidev-code-margin:0px] [--slidev-code-radius:0px] [--slidev-code-background:transparent] [&_pre]:!whitespace-pre-wrap [&_pre]:!break-words [&_pre]:!overflow-visible [&_pre]:!font-normal [&_pre]:!tracking-normal [&_pre]:![font-variation-settings:normal] [&_button]:hidden [&_.shiki-magic-move-item:not(.shiki-magic-move-enter-active):not(.shiki-magic-move-leave-active):not(.shiki-magic-move-move)]:transition-[color,opacity] [&_.shiki-magic-move-item:not(.shiki-magic-move-enter-active):not(.shiki-magic-move-leave-active):not(.shiki-magic-move-move)]:duration-500 [&_.slidev-code-dishonored:not(.shiki-magic-move-leave-to):not(.shiki-magic-move-enter-from)]:opacity-[0.26] [&_.shiki-magic-move-leave-active]:duration-[calc(var(--smm-duration,1000ms)*0.25)] motion-reduce:[&_.shiki-magic-move-item]:duration-0"
    :style="typography"
  >
    <slot />
  </div>
</template>
