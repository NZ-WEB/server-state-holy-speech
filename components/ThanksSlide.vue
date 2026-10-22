<script setup lang="ts">
import PublicImage from './PublicImage.vue'
</script>

<template>
  <!-- Canvas coordinates account for default layout's 80px / 88px inset.
       SlideFrame supplies the shared procedural stars above this backdrop. -->
  <div class="thanks-slide" data-figma-node="99:4903">
    <div class="thanks-backdrop" aria-hidden="true">
      <PublicImage class="thanks-focal" src="/images/figma-thanks-99-4903-focal.svg" width="1600" height="1250" alt="" />
    </div>

    <h1 class="thanks-title font-heading" data-figma-node="99:4907"><span class="thanks-word">Спасибо</span><span class="thanks-space"> </span><span class="thanks-heart">❤️</span></h1>

    <a class="thanks-qr" data-figma-node="99:4908" href="https://t.me/+g25E4B-9SscxOGM6" target="_blank" rel="noopener noreferrer" aria-label="Открыть Telegram-канал «Ну теперь заживём»">
      <PublicImage class="thanks-qr-image" src="/images/server-state-layer-skills-qr.png" width="1184" height="1184" alt="QR-код приглашения в Telegram-канал «Ну теперь заживём» с логотипом в центре" />
    </a>

    <PublicImage class="thanks-brand" data-figma-node="99:4909" src="/images/figma-thanks-99-4903-logo.svg" width="92" height="32.0606" alt="MAGNIT TECH" />
  </div>
</template>

<style scoped>
.thanks-slide { position: absolute; inset: 0; }
.thanks-backdrop {
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
.thanks-focal { position: absolute; left: 1120px; top: -553px; display: block; max-width: none; }
.thanks-title {
  position: absolute;
  left: 534px;
  top: 182px;
  margin: 0;
  color: rgb(255 255 255 / 90%);
  font-size: 0;
  font-weight: 900;
  line-height: 0;
  white-space: nowrap;
}
.thanks-word { font-size: 120px; line-height: 1; letter-spacing: -2.4px; }
.thanks-space { font-size: 70px; line-height: 1; letter-spacing: -1.4px; }
.thanks-heart { font-size: 80px; line-height: 1; letter-spacing: -1.6px; }
.thanks-qr {
  position: absolute;
  left: 705px;
  top: 374px;
  display: block;
  width: 350px;
  height: 348px;
  overflow: hidden;
  border-radius: 24px;
  background: #fff;
}
.thanks-qr-image { display: block; width: 350px; height: 348px; max-width: none; object-fit: contain; }
.thanks-brand { position: absolute; left: 0; top: 887px; display: block; max-width: none; pointer-events: none; }
</style>
