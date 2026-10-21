<script setup lang="ts">
defineProps<{ stage: number }>()

const consequences = [
  {
    title: 'Нежелательная инвалидация',
    description: 'Сбрасываем больше данных, чем изменилось на сервере',
    node: '90:4180',
  },
  {
    title: 'Потеря контроля за кэшом',
    description: 'Непонятно, кто и почему сбросил данные или запустил refetch',
    node: '90:4186',
  },
  {
    title: 'Лишние запросы',
    description: 'Фоновая работа кэша превращается в лишнюю нагрузку',
    node: '90:4192',
  },
] as const
</script>

<template>
  <section class="server-state-consequences" data-node="90:4179" :data-stage="stage" aria-label="Последствия">
    <template v-for="(consequence, index) in consequences" :key="consequence.title">
      <article
        class="consequence-row consequence-reveal"
        :class="{ 'is-visible': stage >= index + 1 }"
        :data-node="consequence.node"
        :data-stage="index + 1"
        :aria-hidden="stage < index + 1"
      >
        <p class="consequence-icon font-heading" aria-hidden="true">➡️</p>
        <div class="consequence-copy font-body">
          <h2 class="consequence-title">{{ consequence.title }}</h2>
          <p class="consequence-description">{{ consequence.description }}</p>
        </div>
      </article>
      <div
        v-if="index < consequences.length - 1"
        class="consequence-separator consequence-reveal"
        :class="{ 'is-visible': stage >= index + 2 }"
        :data-stage="index + 2"
        aria-hidden="true"
      />
    </template>
  </section>
</template>

<style scoped>
.server-state-consequences {
  display: flex;
  width: 1760px;
  flex-direction: column;
  align-items: flex-end;
  gap: 32px;
  overflow: clip;
}

.consequence-row {
  display: flex;
  width: 100%;
  flex-shrink: 0;
  align-items: center;
  gap: 64px;
  word-break: break-word;
}

.consequence-icon {
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

.consequence-copy {
  display: flex;
  width: 1010px;
  flex-shrink: 0;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 8px;
  font-variation-settings: 'YTLC' 500, 'wdth' 100;
}

.consequence-title {
  width: 100%;
  margin: 0;
  color: #fff;
  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}

.consequence-description {
  width: 100%;
  margin: 0;
  color: rgb(255 255 255 / 69%);
  font-size: 30px;
  font-weight: 400;
  line-height: 38px;
}

.consequence-separator {
  width: 1757px;
  height: 2px;
  flex-shrink: 0;
  background: linear-gradient(to right, rgb(255 255 255 / 20%), rgb(255 255 255 / 0%));
}

.consequence-reveal {
  opacity: 0;
  transform: translateY(12px);
  transition: opacity 300ms ease, transform 300ms ease;
  pointer-events: none;
}

.consequence-reveal.is-visible {
  opacity: 1;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  .consequence-reveal {
    transform: none;
    transition: none;
  }
}
</style>
