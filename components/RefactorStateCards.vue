<script setup lang="ts">
const states = [
  { title: 'Local State', description: 'Флаги модалок · состояние компонентов', node: '1:1578' },
  { title: 'Application State', description: 'Активный адрес', node: '1:1575' },
  { title: 'Server State', description: 'Список адресов · магазин · каталог', node: '1:1572' },
] as const
</script>

<template>
  <div class="refactor-state-cards grid grid-cols-3 gap-[32px] font-body leading-[1.2]">
    <article
      v-for="state in states"
      :key="state.title"
      :data-node="state.node"
      class="refactor-state-card relative box-border flex h-[420px] min-w-0 flex-col gap-[40px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[32px] py-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] before:content-[''] before:absolute before:inset-[-1px] before:rounded-[24px] before:pointer-events-none before:p-[1px] before:bg-[linear-gradient(135deg,rgba(255,255,255,0.32),rgba(255,255,255,0.24))] before:[mask:linear-gradient(#fff_0_0)_content-box,linear-gradient(#fff_0_0)] before:![mask-composite:exclude]"
    >
      <h2 class="relative z-1 m-0 w-full font-bold text-[40px] text-white">{{ state.title }}</h2>
      <p class="relative z-1 m-0 w-full font-normal text-[32px] text-secondary">{{ state.description }}</p>
    </article>
  </div>
</template>
