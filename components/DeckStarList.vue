<script setup lang="ts">
import { computed } from 'vue'

const props = withDefaults(defineProps<{
  items: readonly string[]
  variant?: 'stars' | 'notes'
}>(), { variant: 'stars' })

const rows = computed(() => props.items.map(text => {
  const separator = text.indexOf(' – ')
  return {
    text,
    field: separator < 0 ? '' : text.slice(0, separator),
    description: separator < 0 ? '' : text.slice(separator),
  }
}))
</script>

<template>
  <ul class="deck-star-list font-body" :class="{ 'deck-star-list--notes': variant === 'notes' }">
    <li v-for="row in rows" :key="row.text" class="deck-star-list-item">
      <span v-if="variant === 'stars'" class="deck-star-list-marker" aria-hidden="true">✦</span>
      <span v-if="variant === 'notes' && row.field"><span class="notes-field">{{ row.field }}</span><span class="notes-description">{{ row.description }}</span></span>
      <span v-else :class="{ 'notes-field': variant === 'notes' }">{{ row.text }}</span>
    </li>
  </ul>
</template>

<style scoped>
.deck-star-list {
  display: flex;
  flex-direction: column;
  gap: var(--deck-list-gap, 20px);
  margin: 0;
  padding: 0;
  list-style: none;
  color: var(--deck-list-color, rgb(255 255 255 / 90%));
  font-size: var(--deck-list-font-size, 32px);
  font-weight: 400;
  line-height: var(--deck-list-line-height, 42px);
}

.deck-star-list-item {
  display: flex;
  margin: 0;
  min-width: 0;
}

.deck-star-list-marker {
  width: var(--deck-list-marker-width, 44px);
  flex-shrink: 0;
}

.deck-star-list--notes {
  gap: 16px;
  color: #fff;
  font-size: 28px;
  line-height: 1.4;
  font-variation-settings: 'YTLC' 500, 'wdth' 100;
}

.notes-field {
  font-weight: 600;
  line-height: 1.35;
}

.notes-description {
  color: rgb(255 255 255 / 69%);
  font-weight: 400;
  font-style: normal;
}
</style>
