---
theme: none
title: "Клиентский кеш: как держать серверные данные под контролем"
colorSchema: dark
aspectRatio: 16/9
canvasWidth: 1920
fonts:
  sans: Nunito Sans
  local: RF Dewi Extended, Nunito Sans
  provider: none
htmlAttrs:
  lang: ru
defaults:
  layout: default
layout: default
variant: right
showNumbers: false
---

<div class="relative h-full">
  <img class="absolute left-[734px] top-[-170px] w-[1320px] h-[1320px] max-w-none object-cover opacity-75" src="/images/cover-glass-gears.png" alt="" aria-hidden="true">
  <div class="absolute top-[168px] left-0 z-1">
    <h1 class="m-0 w-[925px] font-heading font-black text-[128px] leading-[0.9] tracking-normal">Клиентский<br>кэш</h1>
    <p class="mt-[64px] text-body text-[40px] leading-[1.2]">как держать<br>серверные данные<br>под контролем</p>
  </div>
</div>

---
layout: default
variant: top-right
---

<div class="relative h-full">
  <img class="absolute right-0 bottom-0 w-[935px] h-[1016px] max-w-none object-cover" src="/images/speaker-portrait.png" alt="Евгений Федосеев">
  <div class="absolute top-[240px] left-0">
    <h1 class="m-0 font-heading font-black text-[96px] leading-[0.9] tracking-[-2px]">Евгений<br>Федосеев</h1>
    <div class="inline-flex mt-[63.2px] py-[22px] px-[30px] border-[2px] border-solid border-white/20 rounded-[20px] bg-[linear-gradient(155deg,rgba(255,255,255,0.02),rgba(255,255,255,0.05))] backdrop-blur-[19px]"><p class="text-body text-[32px] leading-[42px] whitespace-nowrap">Frontend Guild Lead в MAGNIT TECH</p></div>
  </div>
</div>

---
layout: image-center
variant: diagonal
image: /images/frontend-meme.png
backgroundImage: /images/frontend-meme-background.png
alt: 'Мем: фронтендер отвлекается на покраску кнопок от стейта, микрофронтендов и утечек памяти'
showLogo: false
showNumbers: false
---

<MemeLabel class="left-[17.121%] top-[13.63636%]">красить кнопки</MemeLabel>
<MemeLabel class="left-[43.747%] top-[4.54545%]">фронтендеры</MemeLabel>
<MemeLabel class="left-[66.847%] top-[16.16162%]" compact>стейт, микрофронты<br>и утечки памяти</MemeLabel>

---
layout: default
variant: diagonal
clicks: 3
---

<h1 class="absolute top-[108px] left-[-6px] m-0 w-[1151px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.9895deg,#fff_1.5437%,#999_99.362%)]">Поговорим о состояниях</h1>

<StateFormula class="absolute top-[252px] left-[-21px]" />

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-[#ed0f00] whitespace-nowrap">B2C сценарий</p>

<h1 class="absolute top-[146px] left-[-5px] m-0 w-[961px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.03633486403604deg,#fff_1.5437%,#999_99.362%)]">Рассмотрим пример</h1>

<ExampleCards class="absolute top-[314px] left-0 w-full" />

---
layout: default
variant: diagonal-left
clicks: 4
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-[#ed0f00]">Реальная жизнь</p>

<h1 class="absolute top-[146px] left-0 m-0 w-[342px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(98.60518deg,#fff_1.5437%,#999_99.362%)]">Адреса</h1>

<div class="absolute top-[298px] left-[-1px] flex w-[469px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 1 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Список адресов</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 2 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Добавление адреса</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 3 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Удаление адреса</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 4 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Выбор активного адреса</span></p>
</div>

<AddressExample class="absolute top-[308px] left-[764px]" />

---
layout: default
variant: diagonal
---

<ShopExample />
