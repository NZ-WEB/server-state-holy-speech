<script setup lang="ts">
import DeckStarList from './DeckStarList.vue'
import PublicImage from './PublicImage.vue'

// Coordinates are relative to default layout's 80px / 88px content inset.
// The shared SlideFrame supplies the procedural StarField above this backdrop.
const contents = [
  'Архитектурный слой',
  'Инструкции по разработке и миграции',
  'Лучшие практики и ограничения',
] as const
</script>

<template>
  <div class="skills-slide" data-figma-node="2438:2127">
    <div class="skills-backdrop" aria-hidden="true">
      <PublicImage class="skills-secondary" src="/images/figma-skills-2438-2127-secondary.svg" width="1300" height="1000" alt="" />
      <PublicImage class="skills-focal" src="/images/figma-skills-2438-2127-focal.svg" width="1600" height="1250" alt="" />
    </div>

    <p class="skills-kicker font-body" data-figma-node="2438:2131">Артефакт</p>
    <h1 class="skills-title font-heading bg-clip-text" data-figma-node="2438:2133">Server State Layer <span class="skills-accent">Skills</span></h1>

    <DeckStarList class="skills-contents" :items="contents" data-figma-node="2438:2146" />

    <a class="skills-qr" data-figma-node="2438:2206" href="https://t.me/+g25E4B-9SscxOGM6" target="_blank" rel="noopener noreferrer" aria-label="Открыть Telegram-канал «Ну теперь заживём»">
      <PublicImage class="skills-qr-image" src="/images/server-state-layer-skills-qr.png" width="1184" height="1184" alt="QR-код приглашения в Telegram-канал «Ну теперь заживём» с логотипом в центре" />
    </a>

    <PublicImage class="skills-brand" data-figma-node="2438:2132" src="/images/figma-skills-2438-2127-logo.svg" width="92" height="32" alt="MAGNIT TECH" />
  </div>
</template>

<style scoped>
.skills-slide { position: absolute; inset: 0; }
.skills-backdrop {
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
.skills-secondary, .skills-focal { position: absolute; display: block; max-width: none; }
.skills-secondary { left: -650px; top: -580px; }
.skills-focal { left: -540px; top: 280px; }
.skills-kicker {
  position: absolute;
  left: -1px;
  top: 0;
  margin: 0;
  color: #ed0f00;
  font-size: 24px;
  font-weight: 700;
  line-height: 1.1;
}
.skills-title {
  position: absolute;
  left: -3px;
  top: 50px;
  margin: 0;
  color: transparent;
  background-image: linear-gradient(115.43885293380305deg, #fff 1.5437%, #999 99.362%);
  font-size: 80px;
  font-weight: 900;
  line-height: 0.9;
  letter-spacing: -1.6px;
  white-space: nowrap;
}
.skills-accent { color: #ed0f00; }
.skills-contents {
  position: absolute;
  left: -1px;
  top: 202px;
  width: 675px;
  --deck-list-font-size: 32px;
  --deck-list-line-height: 42px;
  --deck-list-gap: 20px;
  --deck-list-color: rgb(255 255 255 / 90%);
  --deck-list-marker-width: 44px;
}
.skills-qr {
  position: absolute;
  left: 896px;
  top: 210px;
  display: block;
  width: 624px;
  height: 619px;
  overflow: hidden;
  border-radius: 40px;
  background: #fff;
}
.skills-qr-image { display: block; width: 624px; height: 619px; max-width: none; object-fit: contain; }
.skills-brand { position: absolute; left: 0; top: 888px; display: block; max-width: none; pointer-events: none; }
</style>
