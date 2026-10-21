<script setup lang="ts">
const outcomes = [
  'Рассмотрели пример',
  'Переписали на пинья колада',
  'Меньше ошибок при изменениях',
  'Хэппи энд',
] as const
</script>

<template>
  <div class="refactor-happy-end absolute inset-x-0 top-[202px] h-[682px] font-body" data-node-id="90:3819">
    <ul class="happy-end-outcomes" data-node-id="90:3827">
      <li v-for="outcome in outcomes" :key="outcome" class="happy-end-outcome">
        <span class="happy-end-check" aria-hidden="true">✅</span>
        <span>{{ outcome }}</span>
      </li>
    </ul>
    <PublicImage
      class="happy-end-image"
      src="/images/figma-90-3826-happy-end-2x.png"
      alt="Кот с улыбкой и подписью Happy ending"
      width="1418"
      height="1348"
      data-node-id="90:3826"
    />
  </div>
</template>

<style scoped>
.happy-end-outcomes {
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 676px;
  margin: 0;
  padding: 0;
  list-style: none;
  color: rgb(255 255 255 / 90%);
  font-size: 32px;
  font-weight: 400;
  line-height: 42px;
}

.happy-end-outcome {
  display: flex;
  align-items: center;
  gap: 20px;
  margin: 0;
  white-space: nowrap;
}

.happy-end-check {
  flex: 0 0 28px;
  width: 28px;
  height: 42px;
  font-size: 28px;
}

.happy-end-image {
  position: absolute;
  top: 8px;
  left: 891px;
  display: block;
  width: 709px;
  height: 674px;
  max-width: none;
  border-radius: 32px;
}
</style>
