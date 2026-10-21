<script setup lang="ts">
defineProps<{ stage: number }>()

const consumers = [
  { key: 'addresses-list', position: 'left' },
  { key: 'addresses-list-shared', position: 'right' },
] as const
</script>

<template>
  <div class="shared-query-cache-diagram relative font-body text-white" aria-live="polite">
    <div data-stage="1" class="reveal-stage" :class="{ 'is-hidden': stage < 1 }" :aria-hidden="stage < 1">
      <div data-node="query-cache" class="query-panel cache-panel">
        <p class="panel-title">Query Cache</p>
        <p class="panel-subtitle">['addresses']</p>
      </div>
    </div>

    <div data-stage="2" class="reveal-stage" :class="{ 'is-hidden': stage < 2 }" :aria-hidden="stage < 2">
      <div data-node="api" class="query-panel api-panel">
        <p class="panel-title">API</p>
      </div>
      <PublicImage
        class="connection api-connection" src="/images/query-dedup-figma-api.svg"
        width="18.4099" height="77.25" alt="" aria-hidden="true"
      />
      <p data-label="one-request" class="one-request">один запрос</p>
    </div>

    <div data-stage="3" class="reveal-stage" :class="{ 'is-hidden': stage < 3 }" :aria-hidden="stage < 3">
      <div
        v-for="consumer in consumers" :key="consumer.key" :data-node="consumer.key"
        class="query-panel consumer-panel" :class="consumer.position"
      >
        <p class="panel-title">Addresses List</p>
        <p class="panel-subtitle">useQuery(addresses)</p>
      </div>
      <PublicImage
        class="connection left-connection" src="/images/query-dedup-figma-consumer-left.svg"
        width="398.455" height="89.25" alt="" aria-hidden="true"
      />
      <PublicImage
        class="connection right-connection" src="/images/query-dedup-figma-consumer-right.svg"
        width="397.455" height="89.25" alt="" aria-hidden="true"
      />
    </div>
  </div>
</template>

<style scoped>
.shared-query-cache-diagram {
  width: 1582px;
  height: 644px;
}

.reveal-stage {
  position: absolute;
  inset: 0;
  transition: opacity 500ms ease-out;
}

.is-hidden {
  opacity: 0;
  pointer-events: none;
}

.query-panel {
  position: absolute;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4px;
  width: 775px;
  height: 156px;
  padding: 40px 24px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 24px;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
  overflow: hidden;
  text-align: center;
}

.panel-title,
.panel-subtitle {
  flex-shrink: 0;
  width: 100%;
  margin: 0;
}

.panel-title {
  color: white;
  font-size: 30px;
  font-weight: 700;
  line-height: 38px;
}

.panel-subtitle {
  color: rgba(255, 255, 255, 0.69);
  font-size: 24px;
  font-weight: 400;
  line-height: 1.35;
}

.consumer-panel { top: 0; }
.consumer-panel.left { left: 0; }
.consumer-panel.right { left: 807px; }
.cache-panel { top: 268px; left: 404px; }
.api-panel { top: 524px; left: 404px; height: 120px; }

.connection {
  position: absolute;
  display: block;
  max-width: none;
  pointer-events: none;
}

/* Native SVG export bounds include stroke/arrowhead overhang. */
.left-connection { left: 385.75px; top: 168px; }
.right-connection { left: 797.795px; top: 168px; }
.api-connection { left: 781.79505px; top: 436px; }

.one-request {
  position: absolute;
  top: 459px;
  left: 811px;
  width: 146px;
  margin: 0;
  color: #41e786;
  font-size: 24px;
  font-weight: 700;
  line-height: 1.1;
  text-align: center;
  white-space: nowrap;
}

@media (prefers-reduced-motion: reduce) {
  .reveal-stage { transition: none; }
}
</style>
