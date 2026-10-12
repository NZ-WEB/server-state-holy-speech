<script setup lang="ts">
defineProps<{ compact?: boolean }>()
</script>

<template>
  <span class="meme-label absolute inline-flex items-center justify-center pt-[6px] px-[15px] pb-[10px] rounded-[12px] bg-[#191919] text-white font-body font-bold leading-none text-center whitespace-nowrap" :class="compact ? 'text-[34px]' : 'text-[36px]'"><slot /></span>
</template>
