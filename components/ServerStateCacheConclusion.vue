<script setup lang="ts">
// Keep the conclusion's current copy; the Figma frame supplies its presentation.
const points = [
  {
    index: '01',
    title: 'Проекция',
    description: 'На клиенте хранится копия серверных данных',
    node: '90:3757',
  },
  {
    index: '02',
    title: 'Устаревает',
    description: 'Со временем локальная копия перестаёт соответствовать серверу',
    node: '90:3762',
  },
  {
    index: '03',
    title: 'Инвалидируется',
    description: 'Свежая версия снова загружается из источника истины',
    node: '90:3763',
  },
] as const
</script>

<template>
  <div class="cache-conclusion" aria-label="Свойства Server State">
    <article v-for="point in points" :key="point.index" :data-node="point.node" class="cache-conclusion-card">
      <p class="cache-conclusion-index font-heading font-black">{{ point.index }}</p>
      <div class="cache-conclusion-copy">
        <h2 class="cache-conclusion-title font-heading font-black">{{ point.title }}</h2>
        <p class="cache-conclusion-description font-body">{{ point.description }}</p>
      </div>
    </article>
  </div>
</template>

<style scoped>
.cache-conclusion {
  display: flex;
  gap: 32.333333px;
  width: 1760px;
  height: 399px;
}

.cache-conclusion-card {
  position: relative;
  box-sizing: border-box;
  display: flex;
  flex: 0 0 565px;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  height: 399px;
  padding: 32px;
  border: 1px solid rgb(255 255 255 / 20%);
  border-radius: 32px;
  background: rgb(255 255 255 / 5%);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
}

.cache-conclusion-card::after {
  position: absolute;
  inset: -1px;
  padding: 1px;
  border-radius: inherit;
  background: linear-gradient(135deg, rgb(255 255 255 / 32%), rgb(255 255 255 / 10%) 36%, rgb(255 255 255 / 2%) 70%);
  content: '';
  pointer-events: none;
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
}

.cache-conclusion-index,
.cache-conclusion-title,
.cache-conclusion-description {
  position: relative;
  z-index: 1;
  margin: 0;
  width: 100%;
}

.cache-conclusion-index,
.cache-conclusion-title {
  font-size: 32px;
  line-height: 1.2;
}

.cache-conclusion-index { color: rgb(255 255 255 / 55%); }
.cache-conclusion-title { color: white; }
.cache-conclusion-copy { display: flex; flex-direction: column; gap: 24px; width: 100%; }
.cache-conclusion-description { color: rgb(255 255 255 / 69%); font-size: 28px; font-weight: 400; line-height: 1.35; }
</style>
