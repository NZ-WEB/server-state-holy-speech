<script setup lang="ts">
const capabilities = [
  { node: '90:4238', title: 'Query Options', description: 'конфигурация запросов' },
  { node: '90:4239', title: 'Mutation Options', description: 'конфигурация мутаций' },
  { node: '90:4240', title: 'Cache Service', description: 'управление кэшом' },
] as const
</script>

<template>
  <div class="architecture-conclusion font-body" data-node-id="90:4229">
    <div class="architecture-backdrop" aria-hidden="true">
      <PublicImage class="architecture-secondary" src="/images/figma-90-4229-secondary.svg" width="1300" height="1000" alt="" data-node-id="90:4230" />
      <PublicImage class="architecture-focal" src="/images/figma-90-4229-focal.svg" width="1600" height="1250" alt="" data-node-id="90:4242" />
    </div>

    <p class="architecture-kicker" data-node-id="90:4231">Выводы</p>
    <h1 class="architecture-heading bg-clip-text font-heading font-black" data-node-id="90:4233">Архитектурный слой</h1>

    <div class="architecture-description" data-node-id="90:4241">
      <p>Чтобы контролировать кэш, ключи и инвалидации, </p>
      <p>ограничиваем работу с Server State архитектурным слоем</p>
    </div>

    <section class="architecture-layer" aria-label="Server State Layer" data-node-id="90:4235">
      <h2 class="architecture-layer-title" data-node-id="90:4236">Server State Layer</h2>
      <div class="architecture-capabilities" data-node-id="90:4237">
        <article v-for="capability in capabilities" :key="capability.node" class="architecture-capability" :data-node-id="capability.node">
          <h3 class="architecture-capability-title">{{ capability.title }}</h3>
          <p class="architecture-capability-description">{{ capability.description }}</p>
        </article>
      </div>
    </section>

    <PublicImage class="architecture-logo" src="/images/figma-90-4229-logo.svg" width="92" height="32" alt="MAGNIT TECH" data-node-id="90:4232" />
  </div>
</template>

<style scoped>
/* Coordinates are relative to the default SlideFrame content origin (80, 88). */
.architecture-conclusion {
  position: absolute;
  inset: 0;
  color: white;
}

.architecture-backdrop {
  position: absolute;
  z-index: -1;
  left: -80px;
  top: -88px;
  width: 1920px;
  height: 1080px;
  overflow: hidden;
  background: #101010;
  pointer-events: none;
}

.architecture-secondary,
.architecture-focal,
.architecture-logo {
  position: absolute;
  display: block;
  max-width: none;
  pointer-events: none;
}

.architecture-secondary { left: -650px; top: -580px; }
.architecture-focal { left: -540px; top: 280px; }
.architecture-logo { left: 0; top: 888px; }

.architecture-kicker {
  position: absolute;
  left: -1px;
  top: 0;
  margin: 0;
  color: #ed0f00;
  font-size: 24px;
  font-weight: 700;
  line-height: 1.1;
}

.architecture-heading {
  position: absolute;
  left: 0;
  top: 50px;
  margin: 0;
  color: transparent;
  background: linear-gradient(113.27209169199533deg, #fff 1.5437%, #999 99.362%);
  background-clip: text;
  font-size: 80px;
  line-height: 0.9;
  letter-spacing: -1.6px;
  white-space: nowrap;
}

.architecture-description {
  position: absolute;
  left: 0;
  top: 202px;
  width: 676px;
  color: rgb(255 255 255 / 90%);
  font-size: 28px;
  font-weight: 400;
  line-height: 1.4;
  white-space: pre-wrap;
}

.architecture-description p { margin: 0; }

.architecture-layer {
  position: absolute;
  left: 800px;
  top: 210px;
  box-sizing: border-box;
  display: flex;
  width: 840px;
  height: 606px;
  flex-direction: column;
  align-items: center;
  gap: 24px;
  overflow: hidden;
  padding: 40px 32px;
  border: 1px solid #ff7166;
  border-radius: 32px;
  background: rgb(255 113 102 / 5%);
  text-align: center;
}

.architecture-layer-title {
  width: 100%;
  flex-shrink: 0;
  margin: 0;
  color: #ff7166;
  font-size: 40px;
  font-weight: 700;
  line-height: 1.2;
}

.architecture-capabilities {
  display: flex;
  width: 100%;
  flex-shrink: 0;
  flex-direction: column;
  gap: 16px;
}

.architecture-capability {
  position: relative;
  box-sizing: border-box;
  display: flex;
  width: 100%;
  height: 140px;
  flex-shrink: 0;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 4px;
  overflow: hidden;
  padding: 32px 24px;
  border: 1px solid rgb(16 16 16 / 10%);
  border-radius: 24px;
  background: rgb(255 255 255 / 5%);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
}

/* Match the deck's native-glass reflection without placing the rim outside its clip. */
.architecture-capability::after {
  position: absolute;
  inset: 0;
  z-index: 1;
  padding: 1px;
  border-radius: inherit;
  background: linear-gradient(135deg, rgb(255 255 255 / 32%), rgb(255 255 255 / 10%) 36%, rgb(255 255 255 / 2%) 70%, rgb(255 255 255 / 24%));
  content: '';
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
  pointer-events: none;
}

.architecture-capability-title,
.architecture-capability-description {
  position: relative;
  z-index: 1;
  width: 100%;
  flex-shrink: 0;
  margin: 0;
}

.architecture-capability-title { font-size: 30px; font-weight: 700; line-height: 38px; }
.architecture-capability-description { color: rgb(255 255 255 / 69%); font-size: 24px; font-weight: 400; line-height: 1.35; }
</style>
