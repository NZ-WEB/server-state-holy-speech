<script setup lang="ts">
// Full-canvas coordinates from Figma 90:3977. The slide owns its header/chrome.
const cards = [
  { node: '90:3989', label: 'Компонент 2', x: 542, y: 400 },
  { node: '90:3991', label: 'Query 2', x: 976, y: 400 },
  { node: '90:3993', label: 'Компонент 1', x: 1410, y: 400 },
  { node: '90:3995', label: 'Query Cache', x: 976, y: 576, cache: true },
  { node: '90:3997', label: 'Query 1', x: 542, y: 816 },
  { node: '90:3999', label: 'Query 3', x: 976, y: 816 },
  { node: '90:4001', label: 'Query 4', x: 1410, y: 816 },
] as const

const arrows = [
  { node: '90:4003', file: 'component-2-invalidates' },
  { node: '90:4006', file: 'component-1-invalidates' },
  { node: '90:4011', file: 'cache-query-2' },
  { node: '90:4014', file: 'cache-query-1' },
  { node: '90:4017', file: 'cache-query-3' },
  { node: '90:4020', file: 'cache-query-4' },
] as const
</script>

<template>
  <section class="project-control font-body" aria-label="Компоненты инвалидируют Query Cache, который обновляет четыре query">
    <div class="project-pain" data-node-id="90:3985">
      <p class="pain-item">• Ключи разбросаны по проекту</p>
      <p class="pain-item">• Инвалидации не связаны с мутациями</p>
      <p class="pain-item">• Правила свежести задаются локально</p>
    </div>
    <div
      v-for="card in cards"
      :key="card.node"
      :data-node-id="card.node"
      class="control-card"
      :class="{ 'control-cache': 'cache' in card }"
      :style="{ left: `${card.x}px`, top: `${card.y}px` }"
    >
      <p class="control-card-label">{{ card.label }}</p>
    </div>
    <PublicImage
      v-for="arrow in arrows"
      :key="arrow.node"
      :data-node-id="arrow.node"
      class="control-arrow"
      :src="`/images/figma-90-3977-${arrow.file}.svg`"
      alt=""
      aria-hidden="true"
      width="1920"
      height="1080"
    />
    <p class="invalidate invalidate-left" data-node-id="90:4009">invalidate</p>
    <p class="invalidate invalidate-right" data-node-id="90:4010">invalidate</p>
  </section>
</template>

<style scoped>
.project-control { position: absolute; width: 1920px; height: 1080px; color: #fff; font-variation-settings: 'YTLC' 500, 'wdth' 100; }
.project-pain { position: absolute; left: 108px; top: 320px; display: flex; flex-direction: column; gap: 32px; width: 402px; overflow: hidden; }
.pain-item { flex-shrink: 0; width: 402px; margin: 0; color: rgb(255 255 255 / 69%); font-size: 32px; font-weight: 400; line-height: 1.2; }
.control-card { position: absolute; box-sizing: border-box; display: flex; align-items: center; justify-content: center; width: 402px; height: 112px; overflow: hidden; padding: 24px; border: 1px solid rgb(255 255 255 / 20%); border-radius: 24px; background: rgb(255 255 255 / 5%); backdrop-filter: blur(19px); box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%); }
.control-card-label { flex-shrink: 0; width: 354px; margin: 0; color: #fff; text-align: center; font-size: 32px; font-weight: 700; line-height: 1.2; }
.control-cache { height: 128px; border: 2px solid #ed0f00; }
.control-cache .control-card-label { font-size: 40px; }
.control-arrow { position: absolute; left: 0; top: 0; display: block; max-width: none; pointer-events: none; }
.invalidate { position: absolute; top: 520px; width: 170px; margin: 0; color: #ed0f00; font-size: 24px; font-weight: 700; line-height: 1.2; }
.invalidate-left { left: 804px; }
.invalidate-right { left: 1410px; }
</style>
