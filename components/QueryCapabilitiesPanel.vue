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
    class="query-capabilities-panel box-border flex h-[440px] w-[836px] shrink-0 flex-col gap-[32px] rounded-[24px] border border-solid border-white/20 bg-white/5 p-[40px] font-body leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
  >
    <h2 class="m-0 shrink-0 font-bold text-[40px]" :class="kind === 'query' ? 'text-[#7f9fff]' : 'text-[#e4bd83]'">{{ capabilities[kind].title }}</h2>
    <div class="grid grid-cols-2 gap-x-[24px] gap-y-[32px]">
      <div
        v-for="field in capabilities[kind].fields" :key="field"
        class="box-border flex h-[112px] w-[366px] items-center justify-center rounded-[24px] border-2 border-solid bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
        :class="kind === 'query' ? 'border-[#7f9fff]' : 'border-[#e4bd83]'"
      >
        <p class="m-0 text-center font-bold text-[32px] text-white">{{ field }}</p>
      </div>
    </div>
  </section>
</template>
