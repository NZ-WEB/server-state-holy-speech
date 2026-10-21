<script setup lang="ts">
const invariants = [
  'Автоматическое поддержание инвариантов',
  'Явная модель зависимостей',
  'Меньше ошибок при изменениях',
] as const
</script>

<template>
  <div class="refactor-invariant font-body" data-node="90:3832">
    <ul class="invariant-list" data-node="90:3839">
      <li v-for="invariant in invariants" :key="invariant" class="invariant-row">
        <span class="invariant-check" aria-hidden="true">✅</span>
        <span class="invariant-copy">{{ invariant }}</span>
      </li>
    </ul>
    <div class="invariant-image-slot" data-node="90:3843">
      <PublicImage
        class="invariant-image"
        src="/images/figma-90-3843-invariant-source.png"
        alt="Семь разноцветных шаров связаны в замкнутое кольцо"
        width="1536"
        height="1024"
      />
    </div>
  </div>
</template>

<style scoped>
.refactor-invariant {
  position: absolute;
  width: 1760px;
  height: 675px;
  color: rgb(255 255 255 / 90%);
  font-weight: 400;
}

.invariant-list {
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 20px;
  width: 738px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.invariant-row {
  display: flex;
  align-items: center;
  gap: 20px;
  margin: 0;
  padding: 0;
  line-height: 42px;
}

.invariant-check {
  flex: 0 0 28px;
  width: 28px;
  height: 42px;
  font-size: 28px;
}

.invariant-copy {
  flex: 0 0 auto;
  font-size: 32px;
  white-space: nowrap;
}

.invariant-image-slot {
  position: absolute;
  top: 0;
  left: 891px;
  width: 709px;
  height: 675px;
  overflow: hidden;
  pointer-events: none;
}

.invariant-image {
  position: absolute;
  display: block;
  top: -2.77%;
  left: -32.05%;
  width: 164.11%;
  height: 114.87%;
  max-width: none;
}
</style>
