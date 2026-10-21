<script setup lang="ts">
defineProps<{ stage: number }>()

const principles = [
  {
    icon: '🔑',
    title: 'Контролируем ключи',
    description: 'У каждого домена есть единое место, где описаны query key и query',
    nowrap: false,
    node: '90:4205',
  },
  {
    icon: '📄',
    title: 'Сужаем публичный API',
    description: 'Компоненты работают со сценарием, а не с десятками методов Query Cache',
    nowrap: true,
    node: '90:4211',
  },
  {
    icon: '🎛️',
    title: 'Управляем кэшем явно',
    description: 'Инвалидации, обновления и сбросы имеют доменные имена и одно место вызова',
    nowrap: true,
    node: '90:4217',
  },
  {
    icon: '📌',
    title: 'Фиксируем правила свежести',
    description: 'staleTime и зависимые запросы становятся частью контракта домена',
    nowrap: false,
    node: '90:4223',
  },
] as const
</script>

<template>
  <section class="architecture-principles" data-node="90:4204" :data-stage="stage" aria-label="Решаем архитектурой">
    <template v-for="(principle, index) in principles" :key="principle.title">
      <article
        class="principle-row principle-reveal"
        :class="{ 'is-visible': stage >= index + 1 }"
        :data-node="principle.node"
        :data-stage="index + 1"
        :aria-hidden="stage < index + 1"
      >
        <p class="principle-icon font-heading" aria-hidden="true">{{ principle.icon }}</p>
        <div class="principle-copy font-body">
          <h2 class="principle-title">{{ principle.title }}</h2>
          <p class="principle-description" :class="{ 'principle-description-nowrap': principle.nowrap }">{{ principle.description }}</p>
        </div>
      </article>
      <div
        v-if="index < principles.length - 1"
        class="principle-separator principle-reveal"
        :class="{ 'is-visible': stage >= index + 2 }"
        :data-stage="index + 2"
        aria-hidden="true"
      />
    </template>
  </section>
</template>

<style scoped>
.architecture-principles {
  display: flex;
  width: 1760px;
  flex-direction: column;
  align-items: flex-end;
  gap: 32px;
  overflow: clip;
}

.principle-row {
  display: flex;
  width: 100%;
  flex-shrink: 0;
  align-items: center;
  gap: 64px;
  word-break: break-word;
}

.principle-icon {
  width: 82px;
  height: 95px;
  flex-shrink: 0;
  margin: 0;
  color: #ed0f00;
  font-size: 80px;
  font-weight: 900;
  line-height: 1.15;
  letter-spacing: -1.6px;
}

.principle-copy {
  display: flex;
  width: 1010px;
  flex-shrink: 0;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 8px;
  font-variation-settings: 'YTLC' 500, 'wdth' 100;
}

.principle-title {
  width: 100%;
  margin: 0;
  color: #fff;
  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}

.principle-description {
  width: 100%;
  margin: 0;
  color: rgb(255 255 255 / 69%);
  font-size: 30px;
  font-weight: 400;
  line-height: 38px;
}

.principle-description-nowrap {
  width: auto;
  white-space: nowrap;
}

.principle-separator {
  width: 1757px;
  height: 2px;
  flex-shrink: 0;
  background: linear-gradient(to right, rgb(255 255 255 / 20%), rgb(255 255 255 / 0%));
}

.principle-reveal {
  opacity: 0;
  transform: translateY(12px);
  transition: opacity 300ms ease, transform 300ms ease;
  pointer-events: none;
}

.principle-reveal.is-visible {
  opacity: 1;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  .principle-reveal {
    transform: none;
    transition: none;
  }
}
</style>
