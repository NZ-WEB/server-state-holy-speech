<script setup lang="ts">
import PublicImage from './PublicImage.vue'
</script>

<template>
  <!-- Default layout places this editable content at canvas80,88.
       Its shared SlideFrame supplies procedural stars above the backdrop. -->
  <div class="type-intro" data-figma-node="98:4883">
    <div class="type-backdrop" aria-hidden="true">
      <PublicImage class="type-secondary" src="/images/figma-type-98-4883-secondary.svg" width="1300" height="1000" alt="" />
      <PublicImage class="type-focal" src="/images/figma-type-98-4883-focal.svg" width="1600" height="1250" alt="" />
    </div>

    <p class="type-kicker font-body" data-figma-node="98:4886">Выводы</p>

    <h1 class="type-title font-heading" data-figma-node="98:4888">
      <span class="type-title-main bg-clip-text">Есть такой тип</span>
      <span class="type-title-accent">Server State</span>
    </h1>

    <p class="type-definition font-body" data-figma-node="98:4890">Server State – проекция серверного состояния на&nbsp;клиенте. Она может устареть и&nbsp;не является источником истины</p>

    <PublicImage class="type-brand" data-figma-node="98:4887" src="/images/figma-type-98-4883-logo.svg" width="92" height="32" alt="MAGNIT TECH" />
  </div>
</template>

<style scoped>
.type-intro { position: absolute; inset: 0; }
.type-backdrop {
  position: absolute;
  z-index: -1;
  left: -80px;
  top: -88px;
  width: 1920px;
  height: 1080px;
  overflow: hidden;
  pointer-events: none;
  background: #101010;
}
.type-secondary, .type-focal { position: absolute; display: block; max-width: none; }
.type-secondary { left: -650px; top: -580px; }
.type-focal { left: -540px; top: 280px; }
.type-kicker {
  position: absolute;
  left: -1px;
  top: 52px;
  margin: 0;
  color: #ed0f00;
  font-size: 24px;
  font-weight: 700;
  line-height: 1.1;
}
.type-title {
  position: absolute;
  left: -5px;
  top: 102px;
  width: max-content;
  margin: 0;
  font-size: 80px;
  font-weight: 900;
  line-height: 0.9;
  letter-spacing: -1.6px;
  white-space: nowrap;
}
.type-title-main {
  display: block;
  color: transparent;
  background-image: linear-gradient(98.43160606165243deg, #fff 1.5437%, #999 99.362%);
}
.type-title-accent { display: block; color: #ed0f00; }
.type-definition {
  position: absolute;
  left: 0;
  top: 318px;
  width: 1126px;
  margin: 0;
  color: rgb(255 255 255 / 90%);
  font-size: 40px;
  font-weight: 400;
  line-height: 1.2;
  letter-spacing: 0;
}
.type-brand { position: absolute; left: 0; top: 888px; display: block; max-width: none; pointer-events: none; }
</style>
