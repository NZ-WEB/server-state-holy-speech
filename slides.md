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
alt: "Мем: фронтендер отвлекается на покраску кнопок от стейта, микрофронтендов и утечек памяти"
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

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реальная жизнь</p>

<h1 class="absolute top-[146px] left-[-6px] m-0 w-[372px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(99.347219deg,#fff_1.5437%,#999_99.362%)]">Каталог</h1>

<div class="absolute top-[298px] left-[-1px] flex w-[529px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p class="m-0 flex whitespace-nowrap"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Список товаров</span></p>
  <p class="catalog-dependency m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 4 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'" :aria-hidden="$clicks < 4"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Каталог зависит от магазина</span></p>
</div>

<CatalogExample class="absolute top-[298px] left-[708px]" />

---
layout: image-center
variant: none
image: /images/delete-address-photo-2x.png
backgroundImage: /images/delete-address-background-export.png
alt: "Удаление адреса вызывает каскад инвалидации: активный адрес, магазин, каталог"
showLogo: false
showNumbers: false
class: "[&_figure]:!absolute [&_figure]:!left-[364px] [&_figure]:!top-[224px] [&_figure]:!w-[1030px] [&_figure]:!h-[716px] [&_figure]:!overflow-visible [&_figure>img]:rounded-[32px] [&>div.pointer-events-none>div]:!left-0 [&>div.pointer-events-none>div]:!top-0 [&>div.pointer-events-none>div]:!w-full [&>div.pointer-events-none>div]:!h-full [&>div.pointer-events-none>div]:!blur-0 [&>div.pointer-events-none>div>img]:!rounded-none [&>div.pointer-events-none>div>div]:!hidden"
---

<h1 class="absolute left-[167px] top-[-128px] m-0 w-[698px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Удалить адрес!</h1>

<div class="pointer-events-none absolute left-[-614.91px] top-[61.12px] -z-1 flex h-[846.626px] w-[1154.261px] items-center justify-center" aria-hidden="true">
  <div class="relative h-[587.001px] w-[1033.32px] rotate-[-15.83deg]">
    <img class="absolute left-[-100px] top-[-100px] max-w-none" :src="'/images/delete-address-focal.svg'" alt="">
  </div>
</div>

---
layout: default
variant: cooking
---

<h1 class="absolute left-[-6px] top-[96px] m-0 w-[817px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.87524243018746deg,#fff_1.5437%,#999_99.362%)]">Как это готовить?</h1>

<p class="absolute left-[-2px] top-[200px] m-0 w-[1704px] font-body font-normal text-[32px] leading-[42px] text-accent"><span class="relative top-[1px]">Выглядит сложно даже без кода</span></p>

<img class="cooking-meme absolute left-[538px] top-[247px] w-[1260px] h-[834px] max-w-none object-cover" src="/images/cooking-meme.png" alt="Мужчина разводит руками в недоумении">

<img class="cooking-glass absolute left-[404px] top-[475.745px] w-[553.578px] h-[232.192px] max-w-none origin-top-left rotate-[-8.177960676deg] opacity-85" src="/images/cooking-glass.png" alt="Я просто хотел удалить адрес">

---
layout: default
variant: section-right
---

<img class="absolute left-[838px] top-[62px] w-[934px] h-[981px] max-w-none object-cover opacity-85 pointer-events-none" src="/images/state-types-intro-glass-controls.png" alt="" aria-hidden="true">

<h1 class="absolute left-[-2px] top-[264px] m-0 w-[836px] font-heading font-black text-[120px] leading-[108px] tracking-[-2px] text-heading">Типы<br>состояний</h1>

<div class="absolute left-0 top-[544px] box-border w-[508px] h-[90px] flex items-start px-[30px] py-[22px] border-[2px] border-solid border-white/20 rounded-[20px] bg-[linear-gradient(175deg,rgba(255,255,255,0.01),rgba(255,255,255,0.07))] shadow-[inset_0_1px_1px_rgba(255,255,255,0.08),inset_0_-1px_1px_rgba(255,255,255,0.05)] backdrop-blur-[19px] overflow-hidden">
  <p class="m-0 font-body font-normal text-[32px] leading-[42px] text-body whitespace-nowrap">Local State и Application State</p>
</div>

---
layout: default
variant: diagonal
clicks: 2
---

<div class="absolute left-[-1px] top-[96px] font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</div>
<div class="absolute left-[-6px] top-[146px]">
  <h1 class="m-0 w-max bg-[linear-gradient(110.3224deg,#ffffff_1.5437%,#999999_99.362%)] bg-clip-text font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-transparent whitespace-nowrap">Local и Application</h1>
</div>
<StateTypesCards class="absolute inset-x-0 top-[297.5px]" :local-bullets="['Состояние одного сценария', 'Может жить в компоненте или composable', 'ref / reactive — способы хранения']" :application-bullets="['Состояние нескольких сценариев', 'Живёт на уровне приложения', 'Store – один из способов его хранить']" />

---
layout: default
variant: diagonal
clicks: 18
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</p>

<h1 class="absolute top-[146px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.8048deg,#fff_1.5437%,#999_99.362%)]">Local или Application?</h1>

<div class="absolute inset-x-0 top-[298px] grid grid-cols-[558px_minmax(0,1fr)] gap-[120px] items-start">

<div class="state-quiz-legend flex w-[558px] flex-col gap-[32px] font-body font-normal text-[28px] leading-[1.35] text-body">
  <p class="m-0"><span class="text-[#7f9fff]">Local State</span> – состояние одного<br>UI-сценария или компонента</p>
  <p class="m-0"><span class="text-[#41e786]">Application State</span> – глобальное клиентское состояние, которое разделяют<br>разные части приложения</p>
</div>

<StateQuizCode :answer-clicks="[4, 9, 13, 18]">

````md magic-move {at:2}
```ts {all|1|3-5|all}
const theme = ref<'light' | 'dark'>('light')

function toggleTheme() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
```
```vue {all|2|4|6-8|all}
<script setup lang="ts">
const addressFormDraft = reactive({ street: '', flat: '' })

const isAddressMapExpanded = ref(false)

function expandMap() {
  isAddressMapExpanded.value = true
}
</script>
```
```vue {all|2|4|all}
<script setup lang="ts">
const loginForm = reactive({ login: '', password: '' })

const isPasswordVisible = ref(false)
</script>
```
```ts {all|1|3-5|7|all}
const activeModal = ref<'address' | 'login' | null>(null)

const open = (modal: 'address' | 'login') => {
  activeModal.value = modal
}

const close = () => activeModal.value = null
```
````

</StateQuizCode>

</div>
