<template>
  <div class="project-control-backdrop" aria-hidden="true">
    <PublicImage class="control-secondary" src="/images/figma-90-3977-secondary.svg" alt="" width="1300" height="1100" />
    <PublicImage class="control-focal" src="/images/figma-90-3977-focal.svg" alt="" width="1500" height="1300" />
  </div>
</template>

<style scoped>
.project-control-backdrop {
  position: absolute;
  width: 1920px;
  height: 1080px;
  overflow: hidden;
  background: #101010;
  pointer-events: none;
}
.control-secondary,
.control-focal { position: absolute; display: block; max-width: none; }
.control-secondary { left: 1150px; top: -740px; }
.control-focal { left: -650px; top: 370px; }
</style>
