<script setup lang="ts">
defineProps<{ stage: number }>()
</script>

<template>
  <div class="catalog-key-tree relative h-[660px] w-[1704px] font-body" aria-live="polite">
    <div
      data-node="catalog-prefix" data-stage="1"
      class="absolute left-[434px] top-0 box-border flex h-[112px] w-[836px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="stage >= 1 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :aria-hidden="stage < 1"
    >
      <p class="m-0 text-center font-normal text-[40px] leading-[1.2] text-[#41e786] [font-family:'Roboto_Mono',monospace]">['catalog']</p>
    </div>

    <svg class="pointer-events-none absolute inset-0 h-[660px] w-[1704px] overflow-visible" viewBox="0 0 1704 660" aria-hidden="true">
      <g data-connection="catalog-menu" data-stage="2" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= 2 ? 'opacity-100' : 'opacity-0'">
        <path d="M852 112 V148 H442 Q418 148 418 172 V193" fill="none" stroke="rgba(255,255,255,0.55)" stroke-width="4" stroke-linecap="round" />
        <path d="M406 188 L418 208 L430 188 Z" fill="rgba(255,255,255,0.55)" />
      </g>
      <g data-connection="catalog-store" data-stage="3" class="transition-[opacity,color] duration-500 ease-out motion-reduce:duration-0" :class="[stage >= 3 ? 'opacity-100' : 'opacity-0', stage >= 4 ? 'text-[#41e786]' : 'text-muted']">
        <path d="M852 112 V148 H1262 Q1286 148 1286 172 V193" fill="none" stroke="currentColor" stroke-width="4" stroke-linecap="round" />
        <path d="M1274 188 L1286 208 L1298 188 Z" fill="currentColor" />
      </g>
      <g data-connection="catalog-invalidation" data-stage="4" class="text-[#41e786] transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="stage >= 4 ? 'opacity-100' : 'opacity-0'">
        <path d="M1286 368 V444" fill="none" stroke="currentColor" stroke-width="4" stroke-linecap="round" />
        <path d="M1274 440 L1286 460 L1298 440 Z" fill="currentColor" />
      </g>
    </svg>

    <div
      data-node="catalog-menu" data-stage="2"
      class="absolute left-0 top-[212px] box-border flex h-[144px] w-[836px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="stage >= 2 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :aria-hidden="stage < 2"
    >
      <p class="m-0 text-center font-normal text-[40px] leading-[1.2] text-white [font-family:'Roboto_Mono',monospace]">['catalog', 'menu']</p>
    </div>

    <div
      data-node="catalog-store" data-stage="3" :data-invalidated="stage >= 4"
      class="absolute right-0 top-[212px] box-border flex h-[144px] w-[836px] flex-col items-center justify-center gap-[8px] rounded-[24px] border-2 border-solid bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[opacity,transform,border-color] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="[stage >= 3 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]', stage >= 4 ? 'border-[#41e786]' : 'border-white/20']"
      :aria-hidden="stage < 3"
    >
      <p class="m-0 text-center font-normal text-[40px] leading-[1.2] text-white [font-family:'Roboto_Mono',monospace]">['catalog', storeId]</p>
    </div>

    <div
      data-node="catalog-invalidation" data-stage="4"
      class="absolute right-0 top-[484px] flex w-[836px] flex-col items-center gap-[8px] text-center transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:transform-none"
      :class="stage >= 4 ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-[12px]'"
      :aria-hidden="stage < 4"
    >
      <p class="m-0 w-full font-bold text-[40px] leading-[1.2] text-[#41e786]">invalidate</p>
      <p class="m-0 w-full font-normal text-[32px] leading-[1.2] text-secondary">только каталог выбранного магазина</p>
    </div>
  </div>
</template>
