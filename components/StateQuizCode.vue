<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext } from '@slidev/client'

const props = defineProps<{ answerClicks: number[] }>()
const { $clicks } = useSlideContext()
const answers = ['application', 'local', 'local', 'application'] as const
const exampleIndex = computed(() => {
  const index = props.answerClicks.findIndex(click => $clicks.value <= click)
  return index < 0 ? answers.length - 1 : index
})
const answer = computed(() => answers[exampleIndex.value])
const revealed = computed(() => props.answerClicks.includes($clicks.value))
</script>

<template>
  <div
    class="state-quiz-code relative min-w-0 self-start rounded-[32px] bg-white/5 border border-solid border-[#ed0f00]/25 p-[32px] backdrop-blur-[19px] shadow-[inset_0_1px_1px_rgba(255,255,255,0.08),inset_0_-1px_1px_rgba(255,255,255,0.05)] transition-opacity duration-500 motion-reduce:duration-0 [--slidev-code-font-family:'Roboto_Mono',monospace] [--slidev-code-font-size:27px] [--slidev-code-line-height:32px] [--slidev-code-padding:0px] [--slidev-code-margin:0px] [--slidev-code-radius:0px] [--slidev-code-background:transparent] [&_pre]:!whitespace-pre-wrap [&_pre]:!break-words [&_pre]:!overflow-visible [&_pre]:!font-normal [&_pre]:!tracking-normal [&_pre]:![font-variation-settings:normal] [&_button]:hidden"
    :class="$clicks >= 1 ? 'opacity-100' : 'opacity-0 pointer-events-none'"
    :aria-hidden="$clicks < 1"
  >
    <div class="transition-opacity duration-500 motion-reduce:duration-0" :class="revealed ? 'opacity-55' : 'opacity-100'">
      <slot />
    </div>
    <Transition
      enter-active-class="transition-opacity duration-500 motion-reduce:duration-0"
      leave-active-class="transition-opacity duration-500 motion-reduce:duration-0"
      enter-from-class="opacity-0"
      leave-to-class="opacity-0"
    >
    <div
      v-if="revealed"
      :key="answer"
      class="state-quiz-answer pointer-events-none absolute inset-[-1px] rounded-[32px] border border-solid"
      :class="answer === 'local' ? 'border-[#7f9fff]' : 'border-[#41e786]'"
      role="status"
      :aria-label="answer === 'local' ? 'Local State' : 'Application State'"
    >
      <div v-if="answer === 'local'" class="absolute right-[34.472px] bottom-[14.853px] flex items-center justify-center w-[339.528px] h-[179.147px]">
        <div class="relative w-[324.813px] h-[140.61px] rotate-[-7deg] overflow-hidden">
          <img class="absolute left-[-1.98%] top-[-6.78%] w-[104%] h-[114.5%] max-w-none" src="/images/state-answer-local.png" alt="LOCAL">
        </div>
      </div>
      <div v-else class="absolute right-[34.623px] bottom-[14.091px] flex items-center justify-center w-[565.377px] h-[204.909px]">
        <div class="relative w-[552.605px] h-[138.596px] rotate-[-7deg] overflow-hidden">
          <img class="absolute left-[-1.57%] top-[-18.31%] w-[103.15%] h-[137.09%] max-w-none" src="/images/state-answer-application.png" alt="APPLICATION">
        </div>
      </div>
    </div>
    </Transition>
  </div>
</template>
