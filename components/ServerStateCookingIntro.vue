<template>
  <!-- The backdrop is deliberately a separate z−1 sibling. SlideFrame adds
       the shared procedural StarField above it and below this foreground. -->
  <div class="cooking-backdrop" aria-hidden="true">
    <PublicImage class="cooking-focal" src="/images/figma-95-4829-focal.svg" alt="" width="1520" height="1480" />
    <PublicImage class="cooking-secondary" src="/images/figma-95-4829-secondary.svg" alt="" width="1150" height="1000" />
  </div>
  <h1 class="cooking-title font-heading" data-node-id="95:4833">Как готовить<br>Server State?</h1>
  <PublicImage class="cooking-gears" data-node-id="95:4835" src="/images/cover-glass-gears.png" alt="" aria-hidden="true" width="1174" height="1174" />
  <PublicImage class="cooking-logo" data-node-id="95:4834" src="/images/figma-95-4829-logo.svg" alt="MAGNIT TECH" width="92" height="32" />
</template>

<style scoped>
.cooking-backdrop {
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
.cooking-focal,
.cooking-secondary,
.cooking-gears,
.cooking-logo { position: absolute; display: block; max-width: none; pointer-events: none; }
.cooking-focal { left: 850px; top: -210px; }
.cooking-secondary { left: 1274px; top: -455px; }
.cooking-title {
  position: absolute;
  left: -2px;
  top: 176px;
  width: 968px;
  margin: 0;
  color: #f7f7f7;
  font-size: 120px;
  font-weight: 900;
  line-height: 0.9;
  letter-spacing: -2px;
}
.cooking-gears { left: 983px; top: -254px; object-fit: cover; opacity: 0.75; }
.cooking-logo { left: 0; top: 888px; }
</style>
