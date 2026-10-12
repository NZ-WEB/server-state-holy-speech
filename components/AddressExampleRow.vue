<script setup lang="ts">
defineProps<{
  label: string
  street: string
  details: string
  active: boolean
  showDelete: boolean
}>()
</script>

<template>
  <article
    class="address-example-row box-border flex h-[140px] w-full shrink-0 items-start gap-[16px] overflow-hidden rounded-[24px] border-[2px] border-solid p-[20px] transition-colors duration-500 ease-out motion-reduce:duration-0"
    :class="active ? 'border-[#ed0f00] bg-[rgba(237,15,0,0.05)]' : 'border-white/20 bg-white/5'"
    :data-active="active"
    :aria-label="`${label}: ${street}`"
  >
    <span class="relative block h-[32px] w-[32px] shrink-0" aria-hidden="true">
      <img class="absolute inset-0 block max-w-none transition-opacity duration-500 motion-reduce:duration-0" :class="active ? 'opacity-0' : 'opacity-100'" src="/images/addresses-marker.svg" alt="">
      <img class="absolute inset-0 block max-w-none transition-opacity duration-500 motion-reduce:duration-0" :class="active ? 'opacity-100' : 'opacity-0'" src="/images/addresses-home-active.svg" alt="">
    </span>
    <div class="flex min-w-0 flex-1 flex-col items-start gap-[12px] overflow-hidden">
      <div class="flex h-[24px] w-[596px] items-center gap-[8px] whitespace-nowrap text-[20px] leading-[24px] transition-colors duration-500 motion-reduce:duration-0" :class="active ? 'text-[#ff7166]' : 'text-muted'">
        <span>{{ label }}</span>
        <span v-if="label === 'ДОМ'" class="font-semibold transition-opacity duration-500 motion-reduce:duration-0" :class="active ? 'opacity-100' : 'opacity-0'" :aria-hidden="!active">✓ Активный адрес</span>
      </div>
      <div class="flex flex-col items-start gap-[4px] whitespace-nowrap">
        <p class="m-0 text-[26px] font-bold leading-[32px] text-white">{{ street }}</p>
        <p class="m-0 text-[20px] font-normal leading-[24px] text-white/80">{{ details }}</p>
      </div>
    </div>
    <button
      type="button"
      :tabindex="showDelete ? 0 : -1"
      :aria-label="`Удалить адрес: ${label}`"
      class="relative h-[32px] w-[32px] shrink-0 overflow-hidden border-0 bg-transparent p-0 !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"
      :class="showDelete ? 'opacity-100 translate-y-0' : 'opacity-0 pointer-events-none translate-y-[8px]'"
    >
      <img class="absolute left-[3px] top-[3px] block max-w-none" src="/images/addresses-delete.svg" alt="" aria-hidden="true">
    </button>
  </article>
</template>
