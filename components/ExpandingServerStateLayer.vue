<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{ stage: number }>()
const expanded = computed(() => props.stage >= 1)

const capabilities = [
  { nodeId: '90:3786', title: 'Query Options', description: 'конфигурация запросов' },
  { nodeId: '90:3787', title: 'Mutation Options', description: 'конфигурация мутаций' },
  { nodeId: '90:3788', title: 'Cache Service', description: 'управление кешом' },
] as const

// Figma 90:3793/3794: byte-identical to this existing native-size export.
const arrow = `${import.meta.env.BASE_URL}images/figma-query-reactivity-arrow.svg`
</script>

<template>
  <div
    data-node-id="90:3777"
    class="expanding-server-state-layer font-body"
    role="group"
    aria-label="Addresses Query, Server State Layer, UI"
    :data-expanded="expanded"
  >
    <article data-node="addresses-query" data-node-id="90:3790" class="side-card addresses-card glass-card">
      <p class="card-title">Addresses Query</p>
    </article>

    <section
      data-node="server-state-layer"
      data-node-id="90:3783"
      class="layer-panel"
      :class="{ 'is-expanded': expanded }"
    >
      <h2 data-node-id="90:3784" class="layer-title">Server State Layer</h2>
      <div data-node="layer-capabilities" data-node-id="90:3785" class="layer-capabilities" :aria-hidden="!expanded">
        <article
          v-for="capability in capabilities"
          :key="capability.nodeId"
          :data-node-id="capability.nodeId"
          :data-capability="capability.title"
          class="capability-card glass-card"
        >
          <p class="card-title">{{ capability.title }}</p>
          <p class="card-description">{{ capability.description }}</p>
        </article>
      </div>
    </section>

    <article data-node="ui" data-node-id="90:3792" class="side-card ui-card glass-card">
      <p class="card-title">UI</p>
      <p class="card-description">компоненты</p>
    </article>

    <img data-node-id="90:3793" class="layer-arrow addresses-arrow" :src="arrow" width="34" height="14.7279" alt="" />
    <img data-node-id="90:3794" class="layer-arrow ui-arrow" :src="arrow" width="34" height="14.7279" alt="" />
  </div>
</template>

<style scoped>
.expanding-server-state-layer {
  position: relative;
  width: 1760px;
  height: 607.2px;
  color: white;
}

.glass-card {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4px;
  overflow: hidden;
  padding: 32px 24px;
  border: 1px solid rgb(16 16 16 / 10%);
  border-radius: 24px;
  background: rgb(255 255 255 / 5%);
  text-align: center;
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
}

.side-card {
  position: absolute;
  top: 233px;
  width: 402px;
}

.addresses-card {
  left: 0;
  height: 140px;
  border-color: rgb(255 255 255 / 20%);
}

.ui-card {
  right: 0;
  height: 140.4px;
}

.card-title {
  width: 100%;
  margin: 0;
  font-size: 30px;
  font-weight: 700;
  line-height: 38px;
}

.card-description {
  width: 100%;
  margin: 0;
  color: rgb(255 255 255 / 69%);
  font-size: 24px;
  font-weight: 400;
  line-height: 1.35;
}

.layer-panel {
  position: absolute;
  top: 233px;
  left: 460px;
  box-sizing: border-box;
  width: 840px;
  height: 140px;
  overflow: hidden;
  border: 1px solid #ff7166;
  border-radius: 32px;
  background: rgb(255 113 102 / 5%);
  text-align: center;
  transition: top 700ms ease-in-out, height 700ms ease-in-out;
}

.layer-panel.is-expanded {
  top: 0;
  height: 607.2px;
}

.layer-title {
  position: absolute;
  top: 45px;
  left: 32px;
  width: 774px;
  margin: 0;
  color: #ff7166;
  font-size: 40px;
  font-weight: 700;
  line-height: 48px;
  transition: top 700ms ease-in-out;
}

.is-expanded .layer-title {
  top: 40px;
}

.layer-capabilities {
  position: absolute;
  top: 112px;
  left: 32px;
  display: flex;
  width: 774px;
  flex-direction: column;
  gap: 16px;
  opacity: 0;
  transform: translateY(16px);
  transition: opacity 500ms ease-out, transform 500ms ease-out;
}

.is-expanded .layer-capabilities {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 200ms;
}

.capability-card {
  width: 100%;
  min-height: 140.4px;
  flex: 0 0 140.4px;
}

.layer-arrow {
  position: absolute;
  top: 295.63605px;
  max-width: none;
  pointer-events: none;
}

.addresses-arrow {
  left: 413px;
}

.ui-arrow {
  left: 1313px;
}

@media (prefers-reduced-motion: reduce) {
  .layer-panel,
  .layer-title,
  .layer-capabilities {
    transition: none;
  }
  .layer-capabilities {
    transform: none;
  }
}
</style>
