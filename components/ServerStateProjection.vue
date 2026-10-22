<script setup lang="ts">
defineProps<{ stage: number }>()

const layers = [
  { title: 'UI', description: 'Отображение', border: 'border-[#41e786]', node: '1:1146' },
  { title: 'Проекция', description: 'Frontend', border: 'border-[#e4bd83]', node: '1:1149' },
  { title: 'Состояние', description: 'Backend', border: 'border-[#7f9fff]', node: '1:1152' },
] as const
</script>

<template>
  <div class="server-state-projection absolute left-[896px] top-[288px] flex w-[836px] flex-col gap-[32px] font-body text-center leading-[1.2]">
    <div
      v-for="(layer, index) in layers"
      :key="layer.title"
      :data-node="layer.node"
      :data-stage="index + 1"
      :aria-hidden="stage < index + 1"
      class="projection-layer box-border flex h-[160px] shrink-0 flex-col items-center justify-center gap-[16px] rounded-[24px] border-2 border-solid bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="[layer.border, stage >= index + 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px] pointer-events-none']"
    >
      <p class="m-0 w-full font-bold text-[40px] text-white">{{ layer.title }}</p>
      <p class="m-0 w-full font-normal text-[32px] text-white/69">{{ layer.description }}</p>
    </div>
  </div>
</template>
