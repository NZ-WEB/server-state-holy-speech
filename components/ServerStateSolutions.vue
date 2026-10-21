<template>
  <div class="solutions flex gap-[32px] font-body" data-node-id="89:3469">
    <article class="solution-card" aria-label="TanStack Query">
      <div class="solution-content">
        <div class="solution-tanstack-brand">
          <PublicImage data-node-id="89:3473" class="solution-tanstack-logo" src="/images/figma-89-3473-tanstack-logo.svg" width="252" height="43.7294" alt="TanStack" />
          <p class="solution-query-name">Query</p>
        </div>
        <p class="solution-description" data-node-id="89:3483">Query cache, keys, stale и gc timers, mutations, invalidation, refetch</p>
        <a class="solution-destination solution-destination-query" href="https://tanstack.com/query" target="_blank" rel="noopener noreferrer" data-node-id="89:3484">tanstack.com/query</a>
        <a class="solution-qr" href="https://tanstack.com/query" target="_blank" rel="noopener noreferrer" aria-label="Документация TanStack Query" data-node-id="89:3485">
          <PublicImage class="solution-qr-image" src="/images/figma-89-3486-tanstack-qr.svg" width="269.253" height="269.253" alt="QR-код документации TanStack Query" data-node-id="89:3486" />
        </a>
      </div>
    </article>
    <article class="solution-card" aria-label="Pinia Colada" data-node-id="89:3490">
      <div class="solution-content">
        <div class="solution-colada-brand" data-node-id="89:3494">
          <PublicImage class="solution-colada-logo" src="/images/figma-89-3496-colada-logo.svg" width="36.1745" height="66.0513" alt="" data-node-id="89:3496" />
          <p class="solution-colada-name" data-node-id="89:3539">Pinia Colada</p>
        </div>
        <p class="solution-description" data-node-id="89:3540">Та же модель Server State в экосистеме Vue: queries, mutations и cache entries</p>
        <a class="solution-destination solution-destination-colada" href="https://pinia-colada.esm.dev" target="_blank" rel="noopener noreferrer" data-node-id="89:3541">pinia-colada.esm.dev</a>
        <a class="solution-qr" href="https://pinia-colada.esm.dev" target="_blank" rel="noopener noreferrer" aria-label="Документация Pinia Colada" data-node-id="89:3542">
          <PublicImage class="solution-qr-image" src="/images/figma-89-3543-colada-qr.svg" width="269.255" height="269.255" alt="QR-код документации Pinia Colada" data-node-id="89:3543" />
        </a>
      </div>
    </article>
  </div>
</template>

<style scoped>
@font-face {
  font-family: 'Inter Solutions';
  src: url('/fonts/Inter-figma-solutions-Variable.ttf') format('truetype');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

.solution-card {
  position: relative;
  box-sizing: border-box;
  flex-shrink: 0;
  width: 864px;
  height: 395px;
  padding: 40px;
  overflow: hidden;
  border: 2px solid rgb(255 255 255 / 20%);
  border-radius: 32px;
  background: rgb(255 255 255 / 5%);
  backdrop-filter: blur(19px);
  box-shadow: inset -24px -24px 64px rgb(255 255 255 / 6%), inset 24px 24px 64px rgb(0 0 0 / 40%);
}

.solution-card::after {
  position: absolute;
  inset: -2px;
  padding: 2px;
  border-radius: inherit;
  background: linear-gradient(135deg, rgb(255 255 255 / 50%), transparent 12%, transparent 85%, rgb(255 255 255 / 35%));
  content: '';
  pointer-events: none;
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
}

.solution-content { position: relative; width: 780px; height: 311px; }
.solution-tanstack-brand { position: absolute; top: 0; left: 0; display: flex; align-items: center; gap: 12px; width: 412px; height: 59px; }
.solution-tanstack-logo { display: block; flex-shrink: 0; max-width: none; }
.solution-query-name { margin: 0; color: white; font-family: 'Inter Solutions', sans-serif; font-size: 40px; font-weight: 700; line-height: 1.2; }
.solution-colada-brand { position: absolute; top: 0; left: 0; width: 412px; height: 59px; }
.solution-colada-logo { position: absolute; top: -5.5108px; left: 0.9196px; display: block; max-width: none; }
.solution-colada-name {
  position: absolute;
  top: 3px;
  left: 55px;
  margin: 0;
  color: white;
  font-family: 'Inter Solutions', sans-serif;
  font-size: 44px;
  font-weight: 700;
  font-variation-settings: normal;
  font-optical-sizing: none;
  line-height: 1.2;
  white-space: nowrap;
}
.solution-description {
  position: absolute;
  top: 91px;
  left: 0;
  width: 412px;
  margin: 0;
  color: rgb(255 255 255 / 90%);
  font-size: 28px;
  font-weight: 400;
  line-height: 1.4;
}
.solution-destination {
  position: absolute;
  top: 272px;
  left: 0;
  font-size: 28px;
  font-weight: 400;
  line-height: 1.4;
  text-decoration: none;
  white-space: nowrap;
}
.solution-destination-query { color: #86caa9; }
.solution-destination-colada { color: #e4bd83; }
.solution-qr {
  position: absolute;
  top: 0;
  left: 469px;
  display: block;
  width: 311px;
  height: 311px;
  overflow: hidden;
  border-radius: 25.047px;
  background: white;
}
.solution-qr-image { position: absolute; top: 20.8725px; left: 20.8725px; display: block; max-width: none; }
</style>
