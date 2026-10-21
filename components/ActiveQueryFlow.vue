<script setup lang="ts">
defineProps<{ stage: number }>()

// The first four clicks explain an active query, the next four an inactive one.
// Geometry and copy: Figma 90:3795; visibility is driven only by Slidev's stage.
const rows = [
  [
    { node: '90:3804', stage: 1, title: 'UI-компонент', description: 'читает адреса' },
    { node: '90:3806', stage: 2, title: "Query ['addresses']", description: 'есть подписчик' },
    { node: '90:3808', stage: 3, title: 'invalidate', description: 'кэш устарел' },
    { node: '90:3810', stage: 4, title: 'refetch', description: 'сразу' },
  ],
  [
    { node: '90:3812', stage: 5, title: 'Нет компонента', description: 'никто не\u00a0читает' },
    { node: '90:3814', stage: 6, title: "Query ['catalog']", description: 'нет подписчиков' },
    { node: '90:3816', stage: 7, title: 'invalidate', description: 'кэш устарел' },
    { node: '90:3818', stage: 8, title: 'Ожидание', description: 'до нового подписчика' },
  ],
] as const

// Exported 90:3805 vector is byte-identical to the already downloaded asset.
const arrow = `${import.meta.env.BASE_URL}images/figma-query-reactivity-arrow.svg`
</script>

<template>
  <div class="active-query-flow font-body" :data-stage="stage">
    <div v-for="(row, rowIndex) in rows" :key="rowIndex" class="active-query-row" :data-row="rowIndex">
      <template v-for="(card, columnIndex) in row" :key="card.node">
        <article
          :data-node="card.node"
          :data-stage="card.stage"
          :aria-hidden="stage < card.stage"
          class="active-query-card active-query-reveal"
          :class="{ 'active-query-card-first': columnIndex === 0, 'is-visible': stage >= card.stage }"
        >
          <p class="active-query-title">{{ card.title }}</p>
          <p class="active-query-description">{{ card.description }}</p>
        </article>
        <div
          v-if="columnIndex < row.length - 1"
          class="active-query-arrow active-query-reveal"
          :class="{ 'is-visible': stage >= card.stage + 1 }"
          :data-stage="card.stage + 1"
          :data-connection="`${card.node}-to-${row[columnIndex + 1].node}`"
          aria-hidden="true"
        >
          <img :src="arrow" alt="" width="34" height="14.7279" />
        </div>
      </template>
    </div>
  </div>
</template>

<style scoped>
.active-query-flow {
  width: 1760px;
  display: flex;
  flex-direction: column;
  gap: 31.6px;
}

.active-query-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.active-query-card {
  position: relative;
  box-sizing: border-box;
  display: flex;
  flex: 0 0 402px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4px;
  overflow: hidden;
  padding: 40px 24px;
  border: 1px solid rgb(16 16 16 / 10%);
  border-radius: 24px;
  background: rgb(255 255 255 / 5%);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
  text-align: center;
}

.active-query-card-first {
  border-color: rgb(255 255 255 / 20%);
}

.active-query-card::after {
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

.active-query-title,
.active-query-description {
  flex-shrink: 0;
  width: 100%;
  margin: 0;
  font-variation-settings: 'YTLC' 500, 'wdth' 100;
}

.active-query-title {
  font-size: 30px;
  font-weight: 700;
  line-height: 38px;
  color: #fff;
}

.active-query-description {
  font-size: 24px;
  font-weight: 400;
  line-height: 1.35;
  color: rgb(255 255 255 / 69%);
}

.active-query-arrow {
  position: relative;
  flex: 0 0 32px;
  height: 0;
  pointer-events: none;
}

.active-query-arrow img {
  position: absolute;
  left: -1px;
  top: -7.36395px;
  display: block;
  max-width: none;
}

.active-query-reveal {
  opacity: 0;
  transition: opacity 500ms ease-out;
}

.active-query-reveal.is-visible {
  opacity: 1;
}

@media (prefers-reduced-motion: reduce) {
  .active-query-reveal {
    transition: none;
  }
}
</style>
