<script setup lang="ts">
// Marker exports include their original shadow extents; the labels stay native.
const markers = [
  {
    label: 'Покупатель',
    image: '/images/shop-buyer-background.svg',
    imagePosition: 'left-[360.166992px] top-[505.445801px]',
    labelPosition: 'left-[315.166992px] top-[582.445801px] w-[154px]',
    labelColor: 'bg-canvas text-white',
  },
  {
    label: 'Магазин 1',
    image: '/images/shop-store-1-marker.svg',
    imagePosition: 'left-[886.054688px] top-[337px]',
    labelPosition: 'left-[849.554688px] top-[414px] w-[137px]',
    labelColor: 'bg-white text-canvas',
  },
  {
    label: 'Магазин 3',
    image: '/images/shop-store-3-marker.svg',
    imagePosition: 'left-[985.736328px] top-[568px]',
    labelPosition: 'left-[947.736328px] top-[645px] w-[140px]',
    labelColor: 'bg-white text-canvas',
  },
  {
    label: 'Магазин 2',
    image: '/images/shop-store-2-marker.svg',
    imagePosition: 'left-[1202.103516px] top-[427px]',
    labelPosition: 'left-[1164.103516px] top-[504px] w-[140px]',
    labelColor: 'bg-white text-canvas',
  },
] as const
</script>

<template>
  <div class="shop-example relative h-full">
    <p class="absolute left-[-1px] top-0 font-body font-bold text-[24px] leading-[1.1] text-accent whitespace-nowrap">Реальная жизнь</p>
    <h1 class="absolute left-[-5px] top-[50px] m-0 w-[400px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-transparent bg-clip-text bg-[linear-gradient(100.03695343495372deg,#fff_1.5437%,#999_99.362%)] whitespace-nowrap">Магазин</h1>
    <p class="absolute left-[-2px] top-[194px] w-[1270px] font-body font-normal text-[28px] leading-[1.4] text-body">Ближайший магазин актуален минуту, потом его нужно обновить</p>

    <PublicImage class="absolute left-0 top-[248px] w-[1760px] h-[545px] max-w-none rounded-[32px]" src="/images/shop-map-2x.png" alt="Карта расположения покупателя и трёх магазинов" />

    <template v-for="marker in markers" :key="marker.label">
      <PublicImage class="absolute max-w-none" :class="marker.imagePosition" :src="marker.image" alt="" aria-hidden="true" />
      <div class="absolute flex items-center justify-center h-[40px] pl-[20px] pr-[18px] py-[8px] rounded-[48px] shadow-[0_4px_4px_rgba(0,0,0,0.16),0_0_0.5px_rgba(0,0,0,0.16)]" :class="[marker.labelPosition, marker.labelColor]">
        <span class="font-ui [font-weight:510] text-[20px] leading-[24px] whitespace-nowrap [font-variation-settings:'wdth'_100]">{{ marker.label }}</span>
      </div>
    </template>

    <PublicImage class="absolute left-[385.166992px] top-[563.445801px] max-w-none" src="/images/shop-buyer-dot.svg" alt="" aria-hidden="true" />
    <PublicImage class="absolute left-[380px] top-[520px] max-w-none" src="/images/shop-buyer-person.svg" alt="" aria-hidden="true" />

    <div class="absolute left-[1591px] top-[280px] flex items-center gap-[8px] w-[137px] h-[40px] pl-[12px] pr-[18px] py-[8px] rounded-[48px] bg-black/35 backdrop-blur-[5.95px] shadow-[0_4px_8px_rgba(0,0,0,0.16)] text-light" role="status">
      <span class="relative flex items-center justify-center shrink-0 w-[22px] h-[22px]" aria-hidden="true">
        <span class="relative block w-[19.5px] h-[19.5px]">
          <span class="absolute inset-0 rounded-full bg-[conic-gradient(from_90deg,currentColor_0deg,currentColor_288deg,transparent_288deg)] [mask-image:radial-gradient(circle,transparent_6.75px,#000_6.75px)]"></span>
          <span class="absolute left-[16.5px] top-[8.25px] w-[3px] h-[3px] rounded-full bg-current"></span>
          <span class="absolute left-[10.799px] top-[0.404px] w-[3px] h-[3px] rounded-full bg-current"></span>
        </span>
      </span>
      <span class="font-ui [font-weight:510] text-[16px] leading-[24px] whitespace-nowrap [font-variation-settings:'wdth'_100]">Loading...</span>
    </div>
  </div>
</template>
