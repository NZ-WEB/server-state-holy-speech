<script setup lang="ts">
defineProps<{ items: readonly string[] }>()
</script>

<template>
  <ul class="deck-star-list font-body">
    <li v-for="item in items" :key="item" class="deck-star-list-item">
      <span class="deck-star-list-marker" aria-hidden="true">✦</span>
      <span>{{ item }}</span>
    </li>
  </ul>
</template>

<style scoped>
.deck-star-list {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin: 0;
  padding: 0;
  list-style: none;
  color: rgb(255 255 255 / 90%);
  font-size: 32px;
  font-weight: 400;
  line-height: 42px;
}

.deck-star-list-item {
  display: flex;
  margin: 0;
  min-width: 0;
}

.deck-star-list-marker {
  width: 44px;
  flex-shrink: 0;
}
</style>
