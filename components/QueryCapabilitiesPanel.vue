<script setup lang="ts">
defineProps<{
  kind: 'query' | 'mutation'
}>()

const capabilities = {
  query: { title: 'useQuery', fields: ['data', 'isLoading', 'error', 'refetch'] },
  mutation: { title: 'useMutation', fields: ['mutate', 'isPending', 'error', 'onSuccess'] },
} as const
</script>

<template>
  <section
    :data-node="`${kind}-capabilities`"
    class="query-capabilities-panel box-border flex h-[422px] w-[864px] shrink-0 flex-col gap-[32px] rounded-[32px] border border-solid p-[40px] font-body leading-[1.2]"
    :class="kind === 'query' ? 'border-[#a7b9f4] bg-[rgba(167,185,244,0.05)]' : 'border-[#e4bd83] bg-[rgba(228,189,131,0.05)]'"
  >
    <h2 class="m-0 shrink-0 font-bold text-[40px] leading-[48px] text-white">{{ capabilities[kind].title }}</h2>
    <div class="grid grid-cols-2 gap-[20px]">
      <div
        v-for="field in capabilities[kind].fields" :key="field"
        class="capability-glass-field relative box-border flex h-[120px] w-[381px] items-center justify-center rounded-[24px] border border-solid border-[rgba(16,16,16,0.1)] bg-white/5 px-[24px] py-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
      >
        <p class="m-0 text-center font-normal text-[30px] leading-[38px] text-body">{{ field }}</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.capability-glass-field::after {
  content: '';
  position: absolute;
  inset: -1px;
  border-radius: inherit;
  padding: 1px;
  background: linear-gradient(135deg, rgb(255 255 255 / 32%), rgb(255 255 255 / 10%) 36%, rgb(255 255 255 / 2%) 70%);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
  pointer-events: none;
}
</style>
