<script setup lang="ts">
const capabilities = ['Query Options', 'Mutation Options', 'Cache Service'] as const

const connections = [
  { name: 'query', x1: 644, y1: 146, x2: 273.333333, y2: 331 },
  { name: 'mutation', x1: 852, y1: 146, x2: 852, y2: 331 },
  { name: 'cache', x1: 1060, y1: 146, x2: 1430.666667, y2: 331 },
] as const
</script>

<template>
  <div class="server-state-layer-architecture relative w-[1704px] h-[496px] font-body text-white" role="group" aria-label="Структура Server State Layer">
    <div data-node="server-state-layer" class="absolute top-0 left-[434px] box-border flex w-[836px] h-[144px] items-center justify-center rounded-[24px] border-2 border-solid border-accent bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
      <p class="m-0 w-full text-center font-bold text-[40px] leading-[1.2]">Server State Layer</p>
    </div>

    <svg class="absolute inset-0 pointer-events-none overflow-visible text-accent" width="1704" height="496" viewBox="0 0 1704 496" fill="none" aria-hidden="true">
      <defs>
        <marker id="layer-architecture-arrow" markerWidth="12" markerHeight="12" refX="10" refY="6" orient="auto" markerUnits="userSpaceOnUse">
          <path d="M0 0L12 6L0 12Z" fill="currentColor" />
        </marker>
      </defs>
      <line v-for="connection in connections" :key="connection.name" :data-connection="connection.name" :x1="connection.x1" :y1="connection.y1" :x2="connection.x2" :y2="connection.y2" stroke="currentColor" stroke-width="4" marker-end="url(#layer-architecture-arrow)" />
    </svg>

    <div class="absolute top-[336px] left-0 right-0 grid grid-cols-3 gap-[32px]">
      <article v-for="capability in capabilities" :key="capability" :data-capability="capability" class="box-border flex h-[160px] min-w-0 items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
        <p class="m-0 w-full text-center font-bold text-[32px] leading-[1.2]">{{ capability }}</p>
      </article>
    </div>
  </div>
</template>
