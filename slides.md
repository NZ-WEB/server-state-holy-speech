---
theme: none
title: "Клиентский кеш: как держать серверные данные под контролем"
colorSchema: dark
aspectRatio: 16/9
canvasWidth: 1920
transition:
  name: slide-left
  enterActiveClass: 'transition-[translate] duration-500 ease-in-out motion-reduce:transition-none'
  leaveActiveClass: 'transition-[translate] duration-500 ease-in-out motion-reduce:transition-none'
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

::canvas::

<div class="relative h-full">
  <PublicImage class="absolute left-[734px] top-[-170px] w-[1320px] h-[1320px] max-w-none object-cover opacity-75" src="/images/cover-glass-gears.png" alt="" aria-hidden="true" />
  <div class="absolute top-[168px] left-0 z-1">
    <h1 class="m-0 w-[925px] font-heading font-black text-[128px] leading-[0.9] tracking-normal">Клиентский<br>кеш</h1>
    <p class="mt-[64px] text-body text-[40px] leading-[1.2]">как держать<br>серверные данные<br>под контролем</p>
  </div>
</div>

---
layout: default
variant: top-right
---

::canvas::

<div class="relative h-full">
  <PublicImage class="absolute right-0 bottom-0 w-[935px] h-[1016px] max-w-none object-cover" src="/images/speaker-portrait.png" alt="Евгений Федосеев" />
  <h1 class="absolute top-[240px] left-[-4px] m-0 font-heading font-black text-[96px] leading-[0.9] tracking-[-2px]">Евгений<br>Федосеев</h1>
  <ul class="absolute top-[484px] left-[2px] m-0 flex list-none flex-col gap-[12px] p-0 font-body font-normal text-[32px] leading-[42px] text-body">
    <li class="m-0 whitespace-pre">—&nbsp;&nbsp;8+ лет во фронтенде</li>
    <li class="m-0 whitespace-pre">—&nbsp;&nbsp;лидер фронтенд Гильдии</li>
    <li class="m-0 whitespace-pre">—&nbsp;&nbsp;пишу про фронтенд и процессы</li>
  </ul>
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

<h1 class="absolute top-[20px] left-[-6px] m-0 w-[1151px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.9895deg,#fff_1.5437%,#999_99.362%)]">Поговорим о состояниях</h1>

<StateFormula class="absolute top-[164px] left-[-21px]" />

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-[#ed0f00] whitespace-nowrap">B2C сценарий</p>

<h1 class="absolute top-[50px] left-[-5px] m-0 w-[961px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.03633486403604deg,#fff_1.5437%,#999_99.362%)]">Рассмотрим пример</h1>

<ExampleCards class="absolute top-[218px] left-0 w-full" />

---
layout: default
variant: diagonal-left
clicks: 4
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-[#ed0f00]">Реальная жизнь</p>

<h1 class="absolute top-[58px] left-0 m-0 w-[342px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(98.60518deg,#fff_1.5437%,#999_99.362%)]">Адреса</h1>

<div class="absolute top-[210px] left-[-1px] flex w-[469px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 1 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Список адресов</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 2 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Добавление адреса</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 3 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Удаление адреса</span></p>
  <p class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 4 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Выбор активного адреса</span></p>
</div>

<AddressExample class="absolute top-[220px] left-[764px]" />

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

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реальная жизнь</p>

<h1 class="absolute top-[50px] left-[-6px] m-0 w-[372px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(99.347219deg,#fff_1.5437%,#999_99.362%)]">Каталог</h1>

<div class="absolute top-[202px] left-[-1px] flex w-[529px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p class="m-0 flex whitespace-nowrap"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Список товаров</span></p>
  <p class="catalog-dependency m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none" :class="$clicks >= 4 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none -translate-x-[12px]'" :aria-hidden="$clicks < 4"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Каталог зависит от магазина</span></p>
</div>

<CatalogExample surface="glass" class="absolute top-[210px] left-[708px]" />

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
    <PublicImage class="absolute left-[-100px] top-[-100px] max-w-none" :src="'/images/delete-address-focal.svg'" alt="" />
  </div>
</div>

---
layout: default
variant: cooking
---

<h1 class="absolute left-[-6px] top-[8px] m-0 w-[817px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.87524243018746deg,#fff_1.5437%,#999_99.362%)]">Как это готовить?</h1>

<p class="absolute left-[-2px] top-[112px] m-0 font-body font-normal text-[32px] leading-[42px] text-accent whitespace-nowrap">Выглядит сложно даже без кода</p>

<p class="absolute left-[500px] top-[113.33px] m-0 font-body font-normal text-[35px] leading-[45.938px] text-accent whitespace-nowrap" aria-label="Лицо с моноклем">🧐</p>

<PublicImage class="cooking-meme absolute left-[538px] top-[159px] w-[1260px] h-[834px] max-w-none object-cover" src="/images/cooking-meme.png" alt="Мужчина разводит руками в недоумении" />

<PublicImage class="cooking-glass absolute left-[404px] top-[387.745px] w-[553.578px] h-[232.192px] max-w-none origin-top-left rotate-[-8.177960676deg] opacity-85" src="/images/cooking-glass.png" alt="Я просто хотел удалить адрес" />

---
layout: default
variant: section-right
---

<PublicImage class="absolute left-[838px] top-[-26px] w-[934px] h-[981px] max-w-none object-cover opacity-85 pointer-events-none" src="/images/state-types-intro-glass-controls.png" alt="" aria-hidden="true" />

<h1 class="absolute left-[-2px] top-[176px] m-0 w-[836px] font-heading font-black text-[120px] leading-[108px] tracking-[-2px] text-heading">Типы<br>состояний</h1>

<div class="absolute left-0 top-[456px] box-border w-[508px] h-[90px] flex items-start px-[30px] py-[22px] border-[2px] border-solid border-white/20 rounded-[20px] bg-[linear-gradient(175deg,rgba(255,255,255,0.01),rgba(255,255,255,0.07))] shadow-[inset_0_1px_1px_rgba(255,255,255,0.08),inset_0_-1px_1px_rgba(255,255,255,0.05)] backdrop-blur-[19px] overflow-hidden">
  <p class="m-0 font-body font-normal text-[32px] leading-[42px] text-body whitespace-nowrap">Local State и Application State</p>
</div>

---
layout: default
variant: diagonal
clicks: 2
---

<div class="absolute left-[-1px] top-[8px] font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</div>
<div class="absolute left-[-6px] top-[58px]">
  <h1 class="m-0 w-max bg-[linear-gradient(110.3224deg,#ffffff_1.5437%,#999999_99.362%)] bg-clip-text font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-transparent whitespace-nowrap">Local и Application</h1>
</div>
<StateTypesCards class="absolute inset-x-0 top-[209.5px]" :local-bullets="['Состояние одного сценария', 'Может жить в компоненте или composable', 'ref / reactive — способы хранения']" :application-bullets="['Состояние нескольких сценариев', 'Живёт на уровне приложения', 'Store – один из способов его хранить']" />

---
layout: default
variant: diagonal
clicks: 18
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</p>

<h1 class="absolute top-[58px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.8048deg,#fff_1.5437%,#999_99.362%)]">Local или Application?</h1>

<div class="absolute inset-x-0 top-[210px] grid grid-cols-[558px_minmax(0,1fr)] gap-[120px] items-start">

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

---
layout: default
variant: diagonal-left
clicks: 4
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Local или Application</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.1760574395592deg,#fff_1.5437%,#999_99.362%)]">Список адресов</h1>

<div class="real-case-bullets absolute top-[210px] left-[-1px] flex w-[554px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на сервере</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Меняется by action</span></p>
  <p v-click="4" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется только в адресах</span></p>
</div>

<AddressExample static :active-address="null" class="absolute top-[220px] left-[804px]" />

---
layout: default
variant: diagonal-left
clicks: 3
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[58px] left-[0] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.51865950802929deg,#fff_1.5437%,#999_99.362%)]">Активный адрес</h1>

<div class="real-case-bullets absolute top-[210px] left-[-1px] flex w-[469px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на клиенте</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Меняется со временем</span></p>
  <p v-click="3" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется повсеместно</span></p>
</div>

<AddressExample static class="absolute top-[220px] left-[804px]" />

---
layout: default
variant: diagonal
clicks: 3
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Local или Application</p>

<h1 class="absolute top-[58px] left-[0] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.25069355919166deg,#fff_1.5437%,#999_99.362%)]">А каталог и магазин?</h1>

<div class="real-case-bullets absolute top-[210px] left-[-1px] flex w-[529px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на сервере</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Зависит от выбранного адреса</span></p>
  <p v-click="3" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется не везде</span></p>
</div>

<CatalogExample static class="absolute top-[220px] left-[708px]" />

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(115.04475892308335deg,#fff_1.5437%,#999_99.362%)]">За что мы любим Store</h1>

<StoreBenefitsCards class="absolute inset-x-0 top-[210px]" />

---
layout: default
variant: none
showLogo: false
showNumbers: false
---

::canvas::

<PublicImage class="store-everything-background pointer-events-none absolute left-[-80px] top-0 block h-[1080px] w-[1920px] max-w-none" src="/images/store-everything-meme-background-2x.png" alt="" aria-hidden="true" />

<h1 class="absolute left-[249px] top-[88px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Давайте делать всё в Store!</h1>

<PublicImage class="store-everything-meme absolute left-[462px] top-[232px] block h-[751px] w-[836px] max-w-none object-cover" src="/images/store-everything-meme-2x.png" alt="Вовка в короне рядом с бочкой с надписью STORE" />

---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.1760574395592deg,#fff_1.5437%,#999_99.362%)]">Список адресов</h1>

<div class="store-addresses-content absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">

<div class="store-notes relative left-[-28px] top-[-10px] flex w-[402px] shrink-0 flex-col gap-[16px] font-body font-normal text-[28px] leading-[1.4] text-white/69">
  <p class="m-0 w-[460px]"><span class="font-semibold text-white">addresses</span> – данные</p>
  <p class="m-0 w-[460px]"><span class="font-semibold text-white">isLoading</span> – загрузка</p>
  <p class="m-0 w-[460px]"><span class="font-semibold text-white">error</span> – ошибка</p>
  <p class="m-0 w-[460px]"><span class="font-semibold text-white">loadAddresses</span> – action</p>
</div>

<StoreCodePanel :line-height="32">

````md magic-move
```ts {all|7-9|11-13|15}
import { defineStore } from 'pinia'
import { ref } from 'vue'
import { useAddressesApi } from '@/http-transport/addresses'

export const useAddressesStore = defineStore('addresses', () => {
  const api = useAddressesApi()
  const addresses = ref([])
  const isLoading = ref(false)
  const error = ref(null)

  async function loadAddresses() {
    // ...
  }

  return { addresses, isLoading, error, loadAddresses }
})
```
```ts {all}
async function loadAddresses() {
  isLoading.value = true
  error.value = null

  try {
    const nextAddresses = await api.list()
    addresses.value = [...nextAddresses]
  } catch {
    error.value = 'Не удалось загрузить адреса'
  } finally {
    isLoading.value = false
  }
}
```
````

</StoreCodePanel>

</div>

---
layout: store-code
clicks: 1
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(102.9576450088695deg,#fff_1.5437%,#999_99.362%)]">Все actions</h1>

<div class="store-actions-content absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">

<ul class="store-notes m-0 box-border flex w-[402px] shrink-0 list-disc flex-col gap-[24px] pl-[24px] font-body font-normal text-[30px] leading-[38px] text-white">
  <li class="m-0 pl-[4px]">Добавить адрес</li>
  <li class="m-0 pl-[4px]">Удалить адрес</li>
  <li class="m-0 pl-[4px]">Обновить адрес</li>
</ul>

<StoreCodePanel :line-height="28">

````md magic-move
```ts {all}
import { defineStore } from 'pinia'
import { ref } from 'vue'
import { useAddressesApi } from '@/http-transport/addresses'

export const useAddressesStore = defineStore('addresses', () => {
  ...
  async function loadAddresses() {
    ...
  }
  async function createAddress(dto: CreateAddressDTO) {
    ...
  }
  async function removeAddress(addressId: string) {
    ...
  }
  async function updateAddress(dto: UpdateAddressDTO) {
    ...
  }
})
```
```ts {all}
async function removeAddress(addressId: string) {
  isLoading.value = true
  error.value = null

  try {
    await api.remove(addressId)
    await loadAddresses()
  } catch {
    error.value = 'Не удалось удалить адрес'
  } finally {
    isLoading.value = false
  }
}
```
````

</StoreCodePanel>

</div>

---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.51865950802929deg,#fff_1.5437%,#999_99.362%)]">Активный адрес</h1>

<div class="store-active-address-content absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[8px]">
<div class="store-active-address-notes flex w-[460px] shrink-0 flex-col gap-[24px] font-body text-[30px] leading-[38px] text-body">
  <p class="m-0"><span class="font-bold text-accent">activeAddressId</span> – выбранный ID</p>
  <p class="m-0"><span class="font-bold text-accent">activeAddress</span> – активный адрес</p>
  <p class="m-0"><span class="font-bold text-accent">selectAddress</span> – action выбора</p>
</div>

<StoreCodePanel :line-height="28" class="!px-[16px]">

````md magic-move
```ts {6-7|9-12|15-17|19}
import { defineStore } from 'pinia'
import { computed, ref } from 'vue'
import { useAddressesStore } from './addresses'

export const useActiveAddressStore = defineStore('address-act', () => {
  const addresses = useAddressesStore()
  const activeAddressId = ref(null)

  const activeAddress = computed(() =>
    addresses.addresses.find(
      (address) => address.id === activeAddressId.value,
    ),
  )

  function selectAddress(addressId: string) {
    activeAddressId.value = addressId
  }

  return { activeAddress, activeAddressId, selectAddress }
})
```
````

</StoreCodePanel>
</div>

---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(117.15031701376903deg,#fff_1.5437%,#999_99.362%)]">Актуализация состояния</h1>

<p class="refresh-definition absolute top-[288px] inset-x-[28px] m-0 font-body font-normal text-[40px] leading-[1.2] text-secondary">Refresh – повторное получение данных, чтобы клиентская копия снова соответствовала состоянию на сервере.</p>

<div class="refresh-conditions absolute top-[416px] inset-x-[28px] flex flex-col gap-[16px] font-body">
  <div class="refresh-condition relative flex h-[128px] items-center gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">60 секунд</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[1.2] text-secondary">Магазин обновляется раз в минуту</p>
    <div class="refresh-separator absolute inset-x-0 bottom-0 h-[1px] bg-[#ed0f00]/25" aria-hidden="true"></div>
  </div>
  <div class="refresh-condition relative flex h-[128px] items-center gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">Состояние клиента</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[1.2] text-secondary">Клиенту нужно обновлять состояние</p>
    <div class="refresh-separator absolute inset-x-0 bottom-0 h-[1px] bg-[#ed0f00]/25" aria-hidden="true"></div>
  </div>
  <div class="refresh-condition relative flex h-[128px] items-center gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">Повторный запрос</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[1.2] text-secondary">Обновление нужно запускать автоматически</p>
    <div class="refresh-separator absolute inset-x-0 bottom-0 h-[1px] bg-[#ed0f00]/25" aria-hidden="true"></div>
  </div>
</div>

---
layout: store-code
clicks: 7
---


<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.0792614279172deg,#fff_1.5437%,#999_99.362%)]">Ближайший магазин</h1>

<div class="store-nearest-shop-body absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">
<div class="store-nearest-shop-notes relative left-[-29px] top-[-10px] flex w-[402px] shrink-0 flex-col gap-[16px] font-body font-normal text-[28px] leading-[1.4] text-white/69">
  <p class="m-0 whitespace-nowrap"><span class="font-semibold text-white">store</span> – найденный магазин</p>
  <p class="m-0 whitespace-nowrap"><span class="font-semibold text-white">isLoading</span> – загрузка</p>
  <p class="m-0 whitespace-nowrap"><span class="font-semibold text-white">error</span> – ошибка</p>
</div>

<StoreCodePanel :line-height="28" class="relative top-[-28px]">

````md magic-move
```ts {all|5-7|9-19|21}
export const useActiveStoreStore = defineStore('active-store', () => {
  const address = useActiveAddressStore()
  const api = useStoresApi()

  const store = ref(null)
  const isLoading = ref(false)
  const error = ref(null)

  async function loadNearestStore(addressId: string) {
    isLoading.value = true
    error.value = null
    try {
      store.value = await api.nearest(addressId)
    } catch {
      error.value = 'Не удалось загрузить магазин'
    } finally {
      isLoading.value = false
    }
  }

  return { store, isLoading, error, loadNearestStore }
})
```
```ts {1-11|13-16}
async function loadNearestStore(addressId: string) {
  isLoading.value = true
  error.value = null
  try {
    store.value = await api.nearest(addressId)
  } catch {
    error.value = 'Не удалось загрузить магазин'
  } finally {
    isLoading.value = false
  }
}

watch(
  () => address.activeAddress.id,
  async addressId => loadNearestStore(addressId),
)
```
```ts {1-4|6-9}
watch(
  () => address.activeAddress.id,
  async addressId => loadNearestStore(addressId),
)

window.setInterval(
  () => loadNearestStore(address.activeAddress.id),
  60_000,
)
```
````

</StoreCodePanel>
</div>

---
layout: store-code
variant: risk-left
---

<p class="invalidation-kicker absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent whitespace-nowrap">Реальная жизнь</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(115.33539188446608deg,#fff_1.5437%,#999_99.362%)]">Контроль инвалидации</h1>

<div class="invalidation-clown-crop absolute left-[887px] top-[258px] w-[729px] h-[836px] overflow-hidden rounded-[26.954px] pointer-events-none">
  <PublicImage class="invalidation-clown absolute left-[-37.3327441%] top-[-5.8117626%] w-[174.6654726%] h-[105.8498564%] max-w-none" src="/images/invalidation-clown-personalized.png" alt="Автор доклада в костюме клоуна жонглирует мячами" />
</div>

<div class="invalidation-principles absolute left-0 top-[290px] flex w-[738px] flex-col items-start gap-[20px] font-body font-normal text-[32px] leading-[42px] text-body">
  <div class="invalidation-principle flex items-center gap-[20px]">
    <span class="block h-[42px] w-[28px] shrink-0 text-[28px] leading-[42px]" aria-hidden="true">❌</span>
    <p class="m-0 whitespace-nowrap">Ручное поддержание инвариантов</p>
  </div>
  <div class="invalidation-principle flex items-center gap-[20px]">
    <span class="block h-[42px] w-[28px] shrink-0 text-[28px] leading-[42px]" aria-hidden="true">❌</span>
    <p class="m-0 whitespace-nowrap">Разрозненная логика зависимостей</p>
  </div>
  <div class="invalidation-principle flex items-center gap-[20px]">
    <span class="block h-[42px] w-[28px] shrink-0 text-[28px] leading-[42px]" aria-hidden="true">❌</span>
    <p class="m-0 whitespace-nowrap">Риск рассинхронизации</p>
  </div>
</div>

---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(99.34721910752687deg,#fff_1.5437%,#999_99.362%)]">Каталог</h1>

<div class="store-catalog-body absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">
<div class="store-catalog-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body text-[32px] leading-[1.2] text-white">
  <p class="m-0"><span class="font-bold text-accent">products</span> – данные каталога</p>
  <p class="m-0"><span class="font-bold text-accent">isLoading</span> – загрузка</p>
  <p class="m-0"><span class="font-bold text-accent">error</span> – ошибка</p>
</div>

<StoreCodePanel :line-height="28" class="relative top-[-28px]">

````md magic-move
```ts {5-9|11-13|15-17|19}
import { defineStore } from 'pinia'
import { ref, watch } from 'vue'
import { useActiveStoreStore } from './active-store'

export const useCatalogStore = defineStore('catalog', () => {
  const products = ref([])
  const isLoading = ref(false)
  const error = ref(null)
  const store = useActiveStoreStore()

  async function loadCatalog(storeId: string) {
    // ...
  }

  watch(() => store.store.id, async (storeId) => {
    await loadCatalog(storeId)
  })

  return { products, isLoading, error, loadCatalog }
})
```
````

</StoreCodePanel>
</div>

---
layout: store-code
variant: diagonal
class: "[&.slide-frame_.slide-logo]:!left-[80px] [&.slide-frame_.slide-logo]:!bottom-[72px] [&.slide-frame_.slide-number]:!right-[80px] [&.slide-frame_.slide-number]:!bottom-[66px] [&.slide-frame_.slide-number]:!w-[30px] [&.slide-frame_.slide-number]:!px-[3px]"
---


<p class="absolute top-[88px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы</p>

<h1 class="absolute top-[138px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(114.16457633999747deg,#fff_1.5437%,#999_99.362%)]">Асинхронность watch</h1>

<div class="watch-problems absolute top-[320px] left-[-2px] w-[1760px] flex flex-col gap-[40px] font-body">
  <div class="watch-problem relative flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[8px]">
      <p class="m-0 font-bold text-[32px] leading-[1.1] text-white">Race conditions</p>
      <p class="m-0 font-normal text-[30px] leading-[38px] text-white/69">Старый ответ может прийти позже и перезаписать актуальные данные</p>
    </div>
  </div>
  <div class="self-end h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(to_right,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true"></div>
  <div class="watch-problem relative flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[8px]">
      <p class="m-0 font-bold text-[32px] leading-[1.1] text-white">Неявность</p>
      <p class="m-0 font-normal text-[30px] leading-[38px] text-white/69">Причина запроса спрятана в цепочке реактивных наблюдателей</p>
    </div>
  </div>
  <div class="self-end h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(to_right,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true"></div>
  <div class="watch-problem relative flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[8px]">
      <p class="m-0 font-bold text-[32px] leading-[1.1] text-white">Отмена запросов</p>
      <p class="m-0 font-normal text-[30px] leading-[38px] text-white/69">Очистку таймеров и отмену устаревших запросов пишем вручную</p>
    </div>
  </div>
</div>


---
layout: store-code
variant: diagonal-left
class: "[&.slide-frame_.slide-logo]:!left-[80px] [&.slide-frame_.slide-logo]:!bottom-[72px] [&.slide-frame_.slide-number]:!right-[80px] [&.slide-frame_.slide-number]:!bottom-[66px] [&.slide-frame_.slide-number]:!w-[30px] [&.slide-frame_.slide-number]:!px-[3px]"
---


<p class="absolute top-[88px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы</p>

<h1 class="absolute top-[138px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(102.13636440638527deg,#fff_1.5437%,#999_99.362%)]">Boilerplate</h1>

<ul class="boilerplate-list absolute top-[290px] left-0 m-0 p-0 w-[738px] list-none flex flex-col gap-[20px] font-body font-normal text-[32px] leading-[42px] text-body">
  <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">❌</span><span>Одинаковые CRUD-ы</span></li>
  <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">❌</span><span>Служебные состояния</span></li>
  <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">❌</span><span>Обработка ошибок</span></li>
  <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">❌</span><span>Загрузка из API</span></li>
</ul>

<PublicImage class="boilerplate-iceberg absolute top-[298px] left-[927px] block max-w-none w-[673px] h-[674px] rounded-[32px] object-fill" src="/images/boilerplate-iceberg-updated.png" alt="Айсберг: над водой data, под водой isLoading, error, refetch, fetch, clear" width="1199" height="1312" />

---
layout: store-code
variant: diagonal
class: "[&.slide-frame_.slide-logo]:!left-[80px] [&.slide-frame_.slide-logo]:!bottom-[72px] [&.slide-frame_.slide-number]:!right-[80px] [&.slide-frame_.slide-number]:!bottom-[66px] [&.slide-frame_.slide-number]:!w-[30px] [&.slide-frame_.slide-number]:!px-[3px]"
clicks: 1
---

<p class="absolute top-[88px] left-[0px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Альтернатива Store</p>

<h1 class="absolute top-[138px] left-[-3px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.77354411570731deg,#fff_1.5437%,#999_99.362%)]">Composable</h1>

<div class="composable-body absolute inset-x-0 top-[290px] flex items-start justify-between gap-[32px]">
  <ul class="composable-notes m-0 p-0 list-none flex w-[548px] shrink-0 flex-col gap-[20px] font-body font-normal text-[32px] leading-[42px] text-body">
    <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">✅</span><span>Реализует boilerplate</span></li>
    <li class="m-0 flex items-center gap-[20px]"><span class="w-[28px] h-[42px] shrink-0 text-[28px]" aria-hidden="true">✅</span><span>Скрывает реализацию</span></li>
  </ul>

<StoreCodePanel :line-height="28" class="relative top-[8px] !w-[1180px] !flex-[0_0_1180px] !rounded-[32px]">

````md magic-move
```ts
export function useFetch<T>(request: () => Promise<T>) {
  const data = ref<T>()
  const isLoading = ref(false)
  const error = ref<Error>()

  async function execute() {
    isLoading.value = true
    try { data.value = await request() }
    catch (cause) { error.value = cause as Error }
    finally { isLoading.value = false }
  }

  return { data, isLoading, error, execute }
}
```
```ts
import { useFetch } from '@vueuse/core'

const { data, error, isFetching, execute } = useFetch(
  '/api/addresses',
  { immediate: true },
).json<Address[]>()
```
````

</StoreCodePanel>
</div>

---
layout: default
variant: none
clicks: 3
---

<h1 class="absolute top-[50px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.402686deg,#fff_1.5437%,#999_99.362%)]">Дедупликация запросов</h1>

<RequestDeduplicationDiagram />

---
layout: default
variant: diagonal
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализации</p>

<h1 class="absolute top-[50px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(110.188526deg,#fff_1.5437%,#999_99.362%)]">Store не подходит</h1>

<div class="server-state-store-problems absolute top-[232px] left-[-3px] flex w-[1760px] flex-col gap-[40px] font-body">
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Boilerplate</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Загрузка, ошибки и очистка повторяются в каждом action</p>
    </div>
  </div>
  <div class="ml-[3px] h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(90deg,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true" />
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Нет дедупликации</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Компоненты могут параллельно запросить одни данные</p>
    </div>
  </div>
  <div class="ml-[3px] h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(90deg,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true" />
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Это не кеш</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Нет ключей, свежести и управляемой инвалидации</p>
    </div>
  </div>
</div>

---
layout: default
variant: diagonal
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализации</p>

<h1 class="absolute top-[50px] left-[-3px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.727194deg,#fff_1.5437%,#999_99.362%)]">Composable не подходит</h1>

<div class="composable-limitations absolute top-[232px] left-[-3px] flex w-[1760px] flex-col gap-[40px] font-body">
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Нет дедупликации</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Одинаковые запросы запускаются повторно в разных компонентах</p>
    </div>
  </div>
  <div class="ml-[3px] h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(90deg,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true" />
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Дублирование состояния</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Каждый экземпляр composable хранит собственные данные, загрузку и ошибку</p>
    </div>
  </div>
  <div class="ml-[3px] h-[2px] w-[1757px] shrink-0 bg-[linear-gradient(90deg,rgba(255,255,255,0.2),rgba(255,255,255,0))]" aria-hidden="true" />
  <div class="flex h-[95px] items-center gap-[64px]">
    <p class="m-0 h-[95px] w-[116px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[8px]">
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Сложный refresh</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Интервалы и повторные запросы приходится координировать вручную</p>
    </div>
  </div>
</div>

---
layout: default
variant: none
showLogo: false
showNumbers: false
---

::canvas::

<WhatToDoMeme />

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">B2C сценарий</p>

<h1 class="absolute top-[50px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.932013deg,#fff_1.5437%,#999_99.362%)]">Проблемы состояний</h1>

<StateProblemCards :stage="$clicks" />

---
layout: default
variant: none
clicks: 7
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</p>

<h1 class="absolute top-[50px] left-[-1px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.470623deg,#fff_1.5437%,#999_99.362%)]">Жизненный цикл</h1>

<ClientCacheDiagram :stage="$clicks" />

---
layout: store-code
clicks: 3
---

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.5581102367891deg,#fff_1.5437%,#999_99.362%)]">Это же кеш!</h1>

<div class="projection-notes absolute top-[300px] left-[28px] flex w-[836px] flex-col gap-[32px] font-body font-normal text-[32px] leading-[42px] text-white">
  <p class="m-0">Источник истины находится на сервере</p>
  <p class="m-0">На клиенте хранится только копия</p>
  <p class="m-0">Эта копия может устаревать</p>
</div>

<ServerStateProjection :stage="$clicks" />

---
layout: default
variant: diagonal-left
clicks: 3
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Кеш</p>

<h1 class="absolute top-[50px] left-[-5px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.407038deg,#fff_1.5437%,#999_99.362%)]">Кеш – что за зверь?</h1>

<div class="absolute top-[202px] left-0 flex w-[836px] flex-col gap-[32px] font-body">
  <p class="m-0 text-[30px] leading-[38px] text-white">Кеш – временная копия данных, которая позволяет не обращаться к источнику истины<br>при каждом чтении</p>
  <p class="m-0 text-[24px] leading-[1.35] text-white/69">Ключ кеша – уникальный идентификатор,<br>по которому находим нужную копию данных</p>
</div>

<BackendCacheDiagram class="absolute top-[210px] left-[924px]" />

---
layout: default
variant: diagonal-left
clicks: 4
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Кеш</p>

<h1 class="absolute top-[50px] left-[-5px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.388111deg,#fff_1.5437%,#999_99.362%)]">Инвалидация</h1>

<p class="invalidation-definition absolute top-[202px] left-0 m-0 w-[792px] font-body text-[30px] leading-[38px] text-body">Инвалидация кеша – пометка сохранённых данных как устаревших, после которой следующий потребитель получает свежую версию</p>

<InvalidationFlow class="absolute top-[372px] left-0" :stage="$clicks" />

---
layout: default
variant: diagonal
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Состояния</p>

<h1 class="absolute top-[50px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.916947deg,#fff_1.5437%,#999_99.362%)]">Server State</h1>

<p class="absolute top-[202px] left-[-1px] m-0 w-[836px] font-body text-[30px] leading-[38px] text-body">Server State – проекция серверного состояния на клиенте. Она может устареть и не является источником истины</p>

<div class="state-type-comparison absolute top-[341.5px] left-0 grid w-full grid-cols-3 gap-[32px]">
  <article class="box-border flex h-[228px] flex-col gap-[32px] rounded-[32px] border border-solid border-white/20 bg-white/5 p-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <h2 class="m-0 font-heading font-black text-[32px] leading-[1.2] text-[#7f9fff]">Local State</h2>
    <p class="m-0 font-body text-[28px] leading-[1.4] text-white/69">Composables / hooks<br>Локальное состояние</p>
  </article>
  <article class="box-border flex h-[228px] flex-col gap-[32px] rounded-[32px] border border-solid border-white/20 bg-white/5 p-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <h2 class="m-0 font-heading font-black text-[32px] leading-[1.2] text-[#41e786]">Application State</h2>
    <p class="m-0 font-body text-[28px] leading-[1.4] text-white/69">Store<br>Глобальное состояние</p>
  </article>
  <article class="box-border flex h-[228px] flex-col gap-[32px] rounded-[32px] border border-solid border-white/20 bg-white/5 p-[40px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <h2 class="m-0 font-heading font-black text-[32px] leading-[1.2] text-[#ff7166]">Server State</h2>
    <p class="m-0 font-body text-[28px] leading-[1.4] text-white/69">Проекция серверного состояния<br>на клиенте</p>
  </article>
</div>

---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">02</p>

<h1 class="absolute top-[368px] left-[28px] m-0 w-[836px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-transparent bg-clip-text bg-[linear-gradient(100.47881993614514deg,#fff_1.5437%,#999_99.362%)]">Как готовить<br>Server State?</h1>

<PublicImage class="server-state-chapter-gears absolute top-[80px] left-[920px] block h-[960px] w-[960px] max-w-none object-contain opacity-75 pointer-events-none" src="/images/server-state-chapter-gears.png" alt="" aria-hidden="true" />

---
layout: default
variant: none
showLogo: false
showNumbers: false
---

::canvas::

<PublicImage class="requirements-background pointer-events-none absolute left-[-80px] top-0 block h-[1080px] w-[1920px] max-w-none" src="/images/requirements-meme-background-2x.png" alt="" aria-hidden="true" />

<h1 class="absolute left-[389px] top-[88px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Соберем требования</h1>

<PublicImage class="requirements-meme absolute left-[430px] top-[232px] block h-[720px] w-[898px] max-w-none rounded-[32px] object-cover" src="/images/requirements-meme-2x.png" alt="Спанч Боб разводит руками под радугой" />

---
layout: store-code
clicks: 2
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(106.39648337165877deg,#fff_1.5437%,#999_99.362%)]">Кеш – это кеш!</h1>

<div class="query-mutation-tiles absolute top-[304px] inset-x-[28px] flex gap-[32px] font-body">
  <div data-node="query-definition" class="box-border w-[836px] h-[268px] flex flex-col justify-center gap-[16px] px-[40px] py-[24px] rounded-[24px] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 font-bold text-[40px] leading-[1.2] text-[#41e786]">Query</p>
    <p class="m-0 font-normal text-[32px] leading-[1.2] text-secondary">Ищет запись по ключу. При MISS запрашивает данные у backend.</p>
  </div>
  <div data-node="mutation-definition" class="box-border w-[836px] h-[268px] flex flex-col justify-center gap-[16px] px-[40px] py-[24px] rounded-[24px] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 font-bold text-[40px] leading-[1.2] text-[#e4bd83]">Mutation</p>
    <p class="m-0 font-normal text-[32px] leading-[1.2] text-secondary">Меняет данные на backend, после чего связанный кеш может устареть.</p>
  </div>
</div>

<QueryMutationCache class="absolute top-[700px] left-[28px]" :stage="$clicks" />


---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.96470826850641deg,#fff_1.5437%,#999_99.362%)]">Ключи кеша</h1>

<CatalogKeyTree class="absolute top-[304px] left-[28px]" :stage="$clicks" />


---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.35786726442096deg,#fff_1.5437%,#999_99.362%)]">Долой Boilerplate</h1>

<div class="absolute inset-x-[28px] top-[340px] flex items-start justify-between gap-[32px]">
  <QueryCapabilitiesPanel kind="query" />
  <QueryCapabilitiesPanel kind="mutation" />
</div>


---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.92873093740087deg,#fff_1.5437%,#999_99.362%)]">Реактивность</h1>

<p class="absolute top-[304px] left-[28px] w-[1704px] m-0 font-body font-normal text-[40px] leading-[1.2] text-secondary">Каждый следующий query получает входные данные из предыдущего звена цепочки.</p>

<QueryReactivityChain class="absolute top-[592px] left-[28px]" :stage="$clicks" />


---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(106.51307381726778deg,#fff_1.5437%,#999_99.362%)]">Дедупликация</h1>

<SharedQueryCacheDiagram class="absolute top-[304px] left-[28px]" :stage="$clicks" />


---
layout: store-code
clicks: 5
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.74101414327697deg,#fff_1.5437%,#999_99.362%)]">Что мы <span class="text-accent">хотим</span></h1>

<ServerStateRequirementsTable class="absolute top-[304px] left-[28px]" :stage="$clicks" />


---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.07667407611406deg,#fff_1.5437%,#999_99.362%)]">Решения уже есть!</h1>

<div class="client-cache-solutions absolute top-[304px] inset-x-[28px] flex justify-between gap-[32px] font-body">
  <div data-node="1:1433" class="cache-solution-card relative box-border h-[600px] w-[836px] shrink-0 rounded-[24px] border-2 border-solid border-[#41e786] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <div class="absolute top-[38px] left-[38px] flex h-[96px] w-[756px] items-center">
      <PublicImage src="/images/tanstack-query-logo.svg" class="block max-w-none" alt="TanStack" width="600" height="93.362" />
    </div>
    <div class="absolute top-[166px] left-[38px] flex h-[320px] w-[756px] items-center gap-[24px]">
      <p class="m-0 w-[412px] shrink-0 font-normal text-[32px] leading-[1.2] text-secondary">Query cache, keys, stale и gc timers, mutations, invalidation, refetch.</p>
      <a href="https://tanstack.com/query/latest" target="_blank" rel="noopener noreferrer" class="block h-[320px] w-[320px] shrink-0" aria-label="Документация TanStack Query">
        <PublicImage data-node="1:1447" src="/images/tanstack-query-qr-2x.png" class="block h-[320px] w-[320px] max-w-none" alt="QR-код документации TanStack Query" width="640" height="640" />
      </a>
    </div>
    <a href="https://tanstack.com/query/latest" target="_blank" rel="noopener noreferrer" class="absolute top-[518px] left-[38px] w-[756px] font-bold text-[24px] leading-[1.2] text-[#41e786] no-underline">tanstack.com/query</a>
  </div>
  <div data-node="1:1453" class="cache-solution-card relative box-border h-[600px] w-[836px] shrink-0 rounded-[24px] border-2 border-solid border-[#e4bd83] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <div class="absolute top-[38px] left-[38px] flex h-[96px] w-[756px] items-center gap-[24px]">
      <PublicImage src="/images/pinia-colada-logo.svg" class="block max-w-none" alt="" aria-hidden="true" width="64" height="71.84" />
      <p class="m-0 w-[668px] font-bold text-[40px] leading-[1.2] text-white">Pinia Colada</p>
    </div>
    <div class="absolute top-[166px] left-[38px] flex h-[320px] w-[756px] items-center gap-[24px]">
      <p class="m-0 w-[412px] shrink-0 font-normal text-[32px] leading-[1.2] text-secondary">Та же модель Server State в экосистеме Vue: queries, mutations и cache entries.</p>
      <a href="https://pinia-colada.esm.dev/" target="_blank" rel="noopener noreferrer" class="block h-[320px] w-[320px] shrink-0" aria-label="Документация Pinia Colada">
        <PublicImage data-node="1:1500" src="/images/pinia-colada-qr-2x.png" class="block h-[320px] w-[320px] max-w-none" alt="QR-код документации Pinia Colada" width="640" height="640" />
      </a>
    </div>
    <a href="https://pinia-colada.esm.dev/" target="_blank" rel="noopener noreferrer" class="absolute top-[518px] left-[38px] w-[756px] font-bold text-[24px] leading-[1.2] text-[#e4bd83] no-underline">pinia-colada.esm.dev</a>
  </div>
</div>


---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.48233705006426deg,#fff_1.5437%,#999_99.362%)]">Let's refactor!</h1>

<p class="absolute top-[304px] left-[28px] m-0 w-[836px] font-body font-normal text-[40px] leading-[1.2] text-white">Перепишем всё на Pinia Colada</p>

<figure data-node="rewrite-meme" class="absolute top-[240px] right-[28px] m-0 flex h-[718.263px] w-[836px] flex-col items-center justify-center gap-[24px]">
  <PublicImage class="block w-[836px] h-auto max-w-none shrink-0 rounded-[24px]" src="/images/rewrite-everything.png" alt="Эмоциональный герой мема с поднятой рукой" width="643" height="418" />
  <figcaption class="m-0 shrink-0 text-center font-heading font-black text-[48px] leading-[1.2] text-white">Всё переписать!</figcaption>
</figure>


---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.95433580916409deg,#fff_1.5437%,#999_99.362%)]">Получение адресов</h1>

<div class="refactor-addresses-body absolute inset-x-[28px] top-[272px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
  <div data-node="refactor-addresses-notes" class="mt-[28px] w-[600px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
    <p class="m-0">По шагам переносим загрузку, ошибки и повторный запрос в Server State.</p>
  </div>

<StoreCodePanel data-node="refactor-addresses-code" :font-size="25" :line-height="26">

````md magic-move
```ts {all}
import { ref } from 'vue'
import { addressesApi } from '@http/transport'

const addresses = ref([])
const isLoading = ref(false)
const error = ref(null)

async function loadAddresses() {
  isLoading.value = true
  error.value = null

  try {
    const nextAddresses = await addressesApi.list()
    addresses.value = [...nextAddresses]
  } catch {
    error.value = 'Не удалось загрузить адреса'
  } finally {
    isLoading.value = false
  }
}

return { addresses, isLoading, error, loadAddresses }
```
```ts {all|5|6|7}
import { useQuery } from '@pinia/colada'
import { addressesApi } from '@http/transport'

const query = useQuery({
  key: ['addresses'],
  query: addressesApi.list,
  staleTime: 5 * MINUTE,
})
```
````

</StoreCodePanel>
</div>


---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.95433580916409deg,#fff_1.5437%,#999_99.362%)]">Получение адресов</h1>

<div class="refactor-actions-body absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0" :data-stage="$clicks">
  <div class="refactor-actions-notes w-[600px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
    <p class="m-0">По шагам переносим загрузку, ошибки и повторный запрос в Server State.</p>
  </div>

<StoreCodePanel class="refactor-actions-code relative top-[-28px] max-w-[1270px]">

````md magic-move
```ts {all}
import { defineQueryOptions } from '@pinia/colada'
import { addressesApi } from '@http/transport'

export const addressesQuery = defineQueryOptions(() => ({
  key: ['addresses'],
  query: addressesApi.list,
  staleTime: 5 * MINUTE,
}))
```
```ts {all|1,9|5-8}
import { useQuery } from '@pinia/colada'
import { addressesQuery } from '@serverState/address'

const {
  data: addresses,
  isLoading,
  error,
  refetch,
} = useQuery(addressesQuery)
```
````

</StoreCodePanel>
</div>


---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(110.4115335624527deg,#fff_1.5437%,#999_99.362%)]">Всему своё место</h1>

<RefactorStateCards class="absolute top-[352px] inset-x-[28px]" />


---
layout: store-code
clicks: 7
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.14359990942712deg,#fff_1.5437%,#999_99.362%)]">Получение магазина</h1>

<div data-node="refactor-shop" class="absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
<div class="w-[402px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
  <p class="m-0">Ключ запроса зависит от активного адреса.</p>
</div>

<StoreCodePanel :font-size="24" :line-height="24" class="relative top-[-28px]">

````md magic-move
```ts {all}
import { ref, watch } from 'vue'
import { useActiveAddressStore } from '@stores/active-address'
import { shopsApi } from '@http/transport'

const store = ref(null)
const isLoading = ref(false)
const error = ref(null)
const addressStore = useActiveAddressStore()

async function loadNearestStore() {
  store.value = null
  isLoading.value = true
  error.value = null
  try {
    store.value = await shopsApi.getShop(addressStore.activeAddress.id)
  } catch {
    error.value = 'Не удалось загрузить магазин'
  } finally {
    isLoading.value = false
  }
}

watch(() => addressStore.activeAddress.id, async () => {
  await loadNearestStore()
})
```
```ts {all|3,7|1,8|2,6,10-11|12|13|14}
import { computed } from 'vue'
import { defineQueryOptions } from '@pinia/colada'
import { useActiveAddressStore } from '@stores/active-address'
import { shopsApi } from '@http/transport'

export function useShopQueryOptions() {
  const addressStore = useActiveAddressStore()
  const addressId = computed(() => addressStore.activeAddress.id)

  return {
    activeShop: defineQueryOptions(() => ({
      key: () => ['shops', addressId.value],
      query: () => shopsApi.getShop(addressId.value),
      staleTime: 30 * SECOND,
    })),
  }
}
```
````

</StoreCodePanel>
</div>

---
layout: store-code
clicks: 8
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(112.54071791881543deg,#fff_1.5437%,#999_99.362%)]">Получение каталога</h1>

<div data-node="refactor-catalog" class="absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
<div class="w-[402px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
  <p class="m-0">Ключ запроса зависит от найденного магазина.</p>
</div>

<StoreCodePanel :font-size="27" :line-height="28" class="relative top-[-28px]">

````md magic-move
```ts {all}
import { ref, watch } from 'vue'
import { useActiveStoreStore } from '@stores/active-store'

const products = ref([])
const isLoading = ref(false)
const error = ref(null)
const store = useActiveStoreStore()

async function loadCatalog(storeId: string) {
  // BOILERPLATE
}

watch(() => store.store.id, async (storeId) => {
  await loadCatalog(storeId)
})

return { products, isLoading, error, loadCatalog }
```
```ts {all|2,3,7-8|1,9|2,6,11-12|13|14|15|16}
import { computed } from 'vue'
import { defineQueryOptions, useQuery } from '@pinia/colada'
import { useShopQueryOptions } from '@serverState/shop'
import { catalogApi } from '@http/transport'

export function useCatalogQueryOptions() {
  const { activeShop } = useShopQueryOptions()
  const shop = useQuery(activeShop)
  const shopId = computed(() => shop.data.value?.id)

  return {
    activeCatalog: defineQueryOptions(() => ({
      key: ['catalog', shopId.value],
      query: () => catalogApi.getCatalog(shopId.value!),
      staleTime: 5 * MINUTE,
      enabled: !!shopId.value,
    })),
  }
}
```
````

</StoreCodePanel>
</div>


---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.38043091915237deg,#fff_1.5437%,#999_99.362%)]">Удалим же адрес</h1>

<p data-node="remove-address-description" class="absolute top-[280px] left-[28px] m-0 w-[836px] font-body font-normal text-[40px] leading-[1.2] text-secondary">После удаления кеш адресов инвалидируется и вся цепочка запросов перезагружается</p>

<StoreCodePanel data-node="remove-address-code" :font-size="24" :line-height="24" class="absolute top-[520px] left-[28px] !w-[836px] [&_pre_code]:block motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0">

```ts {all|2,6|2,4,8-9|10-14}
import {
  useMutation, useQueryCache,
} from '@pinia/colada'
import { addressesApi } from '@http/transport'

const queryCache = useQueryCache()

const remove = useMutation({
  mutation: addressesApi.remove,
  onSuccess: () => {
    queryCache.invalidateQueries({
      key: ['addresses'],
    })
  },
})
```

</StoreCodePanel>

<RefactorInvalidationFlow class="absolute top-[272px] left-[896px]" />


---
layout: store-code
variant: risk-left
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.97614104983313deg,#fff_1.5437%,#999_99.362%)]">Да будет инвариант</h1>

<PublicImage data-node="1:433" class="absolute left-[880px] top-[265px] block w-[772px] h-[735px] max-w-none" src="/images/refactor-invariant-ring-2x.png" alt="Семь разноцветных шаров связаны в замкнутое кольцо" width="1544" height="1470" />

<div data-node="1:434" class="absolute left-[28px] top-[300px] flex flex-col items-start gap-[32px] font-body text-[32px] leading-[42px] text-white">
  <div class="flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/refactor-invariant-check.svg" alt="" width="64" height="64" />
    <p class="m-0 whitespace-nowrap">Автоматическое поддержание инвариантов</p>
  </div>
  <div class="flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/refactor-invariant-check.svg" alt="" width="64" height="64" />
    <p class="m-0 whitespace-nowrap">Явная модель зависимостей</p>
  </div>
  <div class="flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/refactor-invariant-check.svg" alt="" width="64" height="64" />
    <p class="m-0 whitespace-nowrap">Меньше ошибок при изменениях</p>
  </div>
</div>


---
layout: store-code
clicks: 8
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 data-node="1:1680" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.15316910001444deg,#fff_1.5437%,#999_99.362%)]">Активный query</h1>

<p data-node="1:1681" class="absolute top-[280px] left-[28px] m-0 w-[1704px] font-body font-normal text-[40px] leading-[1.2] text-secondary">Активный query — тот, у которого сейчас есть хотя бы один подписчик.</p>

<ActiveQueryFlow class="absolute top-[432px] left-[28px]" :stage="$clicks" />


---
layout: store-code
clicks: 5
---

<!-- NEW-FIGMA-146-2082:START -->

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-white">Результаты рефакторинга</h1>

<div class="summary-refactor-results absolute top-[288px] left-[28px] flex w-[1704px] flex-col gap-0 font-body leading-[1.2]" role="table">
  <div v-click="1" data-summary-row="1" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[836px] shrink-0 text-[40px] font-bold text-white" role="cell">Boilerplate – всё</p>
    <p class="m-0 translate-y-[2px] w-[836px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Загрузка, ошибки и повторный запрос уже описаны библиотекой</p>
  </div>
  <div v-click="2" data-summary-row="2" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 -translate-y-[2px] w-[836px] shrink-0 text-[40px] font-bold text-white" role="cell">Дедупликация из коробки</p>
    <p class="m-0 -translate-y-[0.5px] w-[836px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Одинаковые queries разделяют один запрос</p>
  </div>
  <div v-click="3" data-summary-row="3" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[836px] shrink-0 text-[40px] font-bold text-white" role="cell">Кеш – это кеш</p>
    <p class="m-0 translate-y-[0.5px] w-[836px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Ключи, свежесть и инвалидация имеют готовый API</p>
  </div>
  <div v-click="4" data-summary-row="4" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[836px] shrink-0 text-[40px] font-bold text-white" role="cell">Больше возможностей</p>
    <p class="m-0 translate-y-[2px] w-[836px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Фоновые обновления и оптимистичные изменения</p>
  </div>
  <div v-click="5" data-summary-row="5" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 -translate-y-px w-[836px] shrink-0 text-[40px] font-bold text-white" role="cell">Реактивная модель</p>
    <p class="m-0 w-[836px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Query зависят друг от друга и автоматически ждут входные данные</p>
  </div>
</div>

<!-- NEW-FIGMA-146-2082:END -->


---
layout: store-code
---

<!-- NEW-FIGMA-147-2002:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 data-node-id="147:2014" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(120.88926413729571deg,#fff_1.5437%,#999_99.362%)]">Слабые стороны Server State</h1>

<div data-node-id="159:2052" class="server-state-weaknesses absolute top-[280px] left-[28px] flex w-[1704px] flex-col gap-0 font-body [&>div>p]:-translate-y-[4px] [&>div>div.flex]:-translate-y-[3px]">
  <div data-node-id="147:2040" class="relative flex h-[200px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Ключи требуют дисциплины</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Нужно договориться, как называть и собирать query key для каждого среза данных.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node-id="147:2046" class="relative flex h-[200px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Контроль инвалидаций</p>
      <p class="m-0 font-normal text-[32px] text-secondary">После каждой мутации нужно точно определить, какие данные больше нельзя считать свежими.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node-id="147:2052" class="relative flex h-[200px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Широкое API</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Query Cache доступен отовсюду – его легко размазать по компонентам, Store и роутеру.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
</div>
<!-- NEW-FIGMA-147-2002:END -->


---
layout: store-code
---

<!-- NEW-FIGMA-147-2058:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Боль проекта</p>

<h1 data-node-id="147:2070" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.16491593163272deg,#fff_1.5437%,#999_99.362%)]">Контроль теряется</h1>

<div data-node-id="147:2096" class="absolute top-[320px] left-[28px] flex w-[402px] flex-col gap-[32px] font-body font-normal text-[32px] leading-[1.2] text-secondary">
  <p class="m-0">• Ключи разбросаны по проекту</p>
  <p class="m-0">• Инвалидации не связаны с мутациями</p>
  <p class="m-0">• Правила свежести задаются локально</p>
</div>

<div class="project-control-diagram absolute inset-0 font-body text-white" role="group" aria-label="Компоненты инвалидируют Query Cache, который обновляет четыре query">
  <div data-node-id="147:2100" class="absolute top-[400px] left-[462px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Компонент 2</div>
  <div data-node-id="147:2102" class="absolute top-[400px] left-[896px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Query 2</div>
  <div data-node-id="147:2104" class="absolute top-[400px] left-[1330px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Компонент 1</div>
  <div data-node-id="147:2106" class="absolute top-[576px] left-[896px] box-border flex h-[128px] w-[402px] items-center justify-center rounded-[24px] border-2 border-solid border-accent bg-white/5 p-[24px] text-center font-bold text-[40px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Query Cache</div>
  <div data-node-id="147:2108" class="absolute top-[816px] left-[462px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Query 1</div>
  <div data-node-id="147:2110" class="absolute top-[816px] left-[896px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Query 3</div>
  <div data-node-id="147:2112" class="absolute top-[816px] left-[1330px] box-border flex h-[112px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center font-bold text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">Query 4</div>
  <PublicImage data-node-id="147:2114" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/component-2-invalidates.svg" alt="" width="1920" height="1080" />
  <PublicImage data-node-id="147:2117" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/component-1-invalidates.svg" alt="" width="1920" height="1080" />
  <p data-node-id="147:2120" class="absolute top-[520px] left-[724px] m-0 w-[170px] font-bold text-[24px] leading-[1.2] text-accent">invalidate</p>
  <p data-node-id="147:2121" class="absolute top-[520px] left-[1330px] m-0 w-[170px] font-bold text-[24px] leading-[1.2] text-accent">invalidate</p>
  <PublicImage data-node-id="147:2122" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/cache-query-2.svg" alt="" width="1920" height="1080" />
  <PublicImage data-node-id="147:2125" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/cache-query-1.svg" alt="" width="1920" height="1080" />
  <PublicImage data-node-id="147:2128" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/cache-query-3.svg" alt="" width="1920" height="1080" />
  <PublicImage data-node-id="147:2131" class="absolute top-0 left-[-80px] block max-w-none pointer-events-none" src="/images/project-control-arrows/cache-query-4.svg" alt="" width="1920" height="1080" />
</div>
<!-- NEW-FIGMA-147-2058:END -->


---
layout: store-code
---

<!-- NEW-FIGMA-1-1825:START -->
<p data-node="1:1829" class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Боль проекта</p>

<h1 data-node="1:1832" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.08129053889449deg,#fff_1.5437%,#999_99.362%)]">Последствия</h1>

<div data-node="1:1833" class="absolute top-[280px] inset-x-[28px] flex flex-col gap-0 font-body [&>div>p]:-translate-y-[4px] [&>div>div.flex]:-translate-y-[3px]">
  <div data-node="1:1834" class="relative flex h-[200px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Нежелательная инвалидация</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Сбрасываем больше данных, чем изменилось на сервере.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node="1:1840" class="relative flex h-[200px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Потеря контроля за кешом</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Непонятно, кто и почему сбросил данные или запустил refetch.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node="1:1846" class="relative flex h-[200px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Лишние запросы</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Фоновая работа кеша превращается в мусорные запросы и лишнюю нагрузку.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
</div>
<!-- NEW-FIGMA-1-1825:END -->


---
layout: store-code
---

<!-- NEW-FIGMA-1-1852:START -->
<p data-node="1:1853" class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 data-node="1:1855" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-white">Решаем архитектурой</h1>

<div data-node="1:1856" class="architecture-principles absolute top-[272px] left-[28px] flex w-[1704px] flex-col gap-0 font-body [&>div>p]:-translate-y-[4px] [&>div>div.flex]:-translate-y-[3px]">
  <div data-node="1:1857" class="relative flex h-[160px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Контролируем ключи</p>
      <p class="m-0 font-normal text-[32px] text-secondary">У каждого домена есть единое место, где описаны query key и query.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node="1:1863" class="relative flex h-[160px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Сужаем публичный API</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Компоненты работают со сценарием, а не с десятками методов Query Cache.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node="1:1869" class="relative flex h-[160px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Управляем кешем явно</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Инвалидации, обновления и сбросы имеют доменные имена и одно место вызова.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div data-node="1:1875" class="relative flex h-[160px] shrink-0 items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">04</p>
    <div class="flex min-w-0 flex-1 flex-col gap-[16px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Фиксируем правила свежести</p>
      <p class="m-0 font-normal text-[32px] text-secondary">staleTime и зависимые запросы становятся частью контракта домена.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
</div>
<!-- NEW-FIGMA-1-1852:END -->


---
layout: store-code
clicks: 1
---

<!-- NEW-FIGMA-1-1882:START -->

<p data-node="1:1886" class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 data-node="1:1889" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(110.1661906828467deg,#fff_1.5437%,#999_99.362%)]">Server State Layer</h1>

<ExpandingServerStateLayer class="absolute top-[304px] left-[28px]" :stage="$clicks" />

<!-- NEW-FIGMA-1-1882:END -->


---
layout: store-code
---

<!-- NEW-FIGMA-1-1912:START -->

<p data-node="1:1916" class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 data-node="1:1919" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(107.74015827818073deg,#fff_1.5437%,#999_99.362%)]">Структура слоя</h1>

<ServerStateLayerArchitecture class="absolute top-[304px] left-[28px]" />

<!-- NEW-FIGMA-1-1912:END -->


---
layout: store-code
clicks: 9
---

<!-- ARCHITECTURE-CODE-62:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.76449780050385deg,#fff_1.5437%,#999_99.362%)]">Query Options</h1>

<div class="architecture-code-body absolute inset-x-[28px] top-[272px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <ul data-node="architecture-notes" class="m-0 mt-[28px] pl-[32px] box-border list-disc flex w-[402px] shrink-0 flex-col gap-[24px] font-body font-normal text-[32px] leading-[1.2] text-secondary">
    <li class="m-0 pl-[4px]">Все Query Options домена адресов храним в одном месте</li>
    <li class="m-0 pl-[4px]">Описываем конфигурацию queries</li>
    <li class="m-0 pl-[4px]">Отвечаем на вопрос: «как делать»</li>
  </ul>

<StoreCodePanel data-node="architecture-code" :font-size="27" :line-height="28" class="max-w-[1270px] [&_pre.shiki]:!whitespace-pre [&_pre]:![--smm-delay-container:0] [&_pre]:![--smm-delay-move:0] [&_pre]:![--smm-delay-enter:0.7] [&_pre]:![--smm-delay-leave:0] [&_pre]:![--smm-easing:ease-in-out] [&_.shiki-magic-move-item]:![--smm-stagger:0ms] [&_.shiki-magic-move-enter-active]:!duration-[calc(var(--smm-duration)*0.25)]">

````md magic-move {duration:1200}
```ts {4|5-9|11}
import { defineQueryOptions } from '@pinia/colada'
import { fetchAddressList } from '@http/transport'

export function useAddressesQueryOptions() {
  const list = defineQueryOptions({
    key: ['addresses'],
    query: fetchAddressList,
    staleTime: 30_000,
  })

  return { list }
}
```
```ts {all|4|5}
import { useAddressesQueryOptions } from '@serverState/address'
import { useQuery } from '@pinia/colada'

const addressQueryOptions = useAddressesQueryOptions()
const addressListQuery = useQuery(addressQueryOptions.list)
```
```ts {all|5|6|7}
import { useAddressesQueryOptions } from '@serverState/address'
import { useQueryCache } from '@pinia/colada'

// Prefetch
const addressQueryOptions = useAddressesQueryOptions()
const queryCache = useQueryCache()
await queryCache.refresh(queryCache.ensure(addressQueryOptions.list))
```
````

</StoreCodePanel>
</div>
<!-- ARCHITECTURE-CODE-62:END -->


---
layout: store-code
clicks: 12
---

<!-- ARCHITECTURE-CODE-63:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.85989467988094deg,#fff_1.5437%,#999_99.362%)]">Mutation Options</h1>

<div class="architecture-code-body absolute inset-x-[28px] top-[272px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <ul data-node="architecture-notes" class="m-0 mt-[28px] pl-[32px] box-border list-disc flex w-[402px] shrink-0 flex-col gap-[24px] font-body font-normal text-[32px] leading-[1.2] text-secondary">
    <li class="m-0 pl-[4px]">Операции записи домена адресов – в одном composable</li>
    <li class="m-0 pl-[4px]">createAddress,<br>updateAddress,<br>removeAddress</li>
    <li class="m-0 pl-[4px]">defineMutationOptions связывает mutation с последствиями успеха</li>
  </ul>

<StoreCodePanel data-node="architecture-code" :font-size="27" :line-height="27" class="max-w-[1270px] [&_pre.shiki]:!whitespace-pre [&_pre]:![--smm-delay-container:0] [&_pre]:![--smm-delay-move:0] [&_pre]:![--smm-delay-enter:0.7] [&_pre]:![--smm-delay-leave:0] [&_pre]:![--smm-easing:ease-in-out] [&_.shiki-magic-move-item]:![--smm-stagger:0ms] [&_.shiki-magic-move-enter-active]:!duration-[calc(var(--smm-duration)*0.25)]">

````md magic-move {duration:1200}
```ts {6|7|9-12|11|13-16|15|17-20|19}
import { defineMutationOptions } from '@pinia/colada'
import { useAddressesApi } from '@http/transport'
import { useAddressesCacheService } from '@serverState/address'

export function useAddressesMutationOptions() {
  const addressesApi = useAddressesApi()
  const cache = useAddressesCacheService()

  const create = defineMutationOptions({
    mutation: addressesApi.create,
    onSuccess: cache.invalidateAddressList,
  })
  const update = defineMutationOptions({
    mutation: addressesApi.update,
    onSuccess: cache.invalidateAddressList,
  })
  const remove = defineMutationOptions({
    mutation: addressesApi.remove,
    onSuccess: cache.invalidateAddressList,
  })

  return { create, update, remove }
}
```
```ts {all|7-8|12|13|15}
import { useAddressesMutationOptions } from '@serverState/address'
import { useMutation } from '@pinia/colada'
import { useRouter } from 'vue-router'
import { toast } from '@ui/toast'

const router = useRouter()
const { remove: removeAddress } = useAddressesMutationOptions()
const { mutateAsync, isLoading } = useMutation(removeAddress)

const handleRemove = async () => {
  try {
    await mutateAsync()
    router.push({ name: 'home' })
  } catch {
    toast('Что-то пошло не так')
  }
}
```
````

</StoreCodePanel>
</div>
<!-- ARCHITECTURE-CODE-63:END -->


---
layout: store-code
clicks: 9
---

<!-- ARCHITECTURE-CODE-64:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.78797602456692deg,#fff_1.5437%,#999_99.362%)]">Cache Service</h1>

<div class="architecture-code-body absolute inset-x-[28px] top-[272px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <ul data-node="architecture-notes" class="m-0 mt-[28px] pl-[32px] box-border list-disc flex w-[402px] shrink-0 flex-col gap-[24px] font-body font-normal text-[32px] leading-[1.2] text-secondary">
    <li class="m-0 pl-[4px]">Все операции с кешем домена адресов живут в одном месте</li>
    <li class="m-0 pl-[4px]">Мутации и компоненты не знают деталей QueryCache</li>
    <li class="m-0 pl-[4px]">Сервис даёт инвалидации понятные доменные имена</li>
  </ul>

<StoreCodePanel data-node="architecture-code" :font-size="27" :line-height="28" class="max-w-[1270px] [&_pre.shiki]:!whitespace-pre [&_pre]:![--smm-delay-container:0] [&_pre]:![--smm-delay-move:0] [&_pre]:![--smm-delay-enter:0.7] [&_pre]:![--smm-delay-leave:0] [&_pre]:![--smm-easing:ease-in-out] [&_.shiki-magic-move-item]:![--smm-stagger:0ms] [&_.shiki-magic-move-enter-active]:!duration-[calc(var(--smm-duration)*0.25)]">

````md magic-move {duration:1200}
```ts {6-7|9-11|12-14|15-17|19}
import { useQueryCache } from '@pinia/colada'
import { useAddressesQueryOptions } from '@serverState/address'
import type { Address } from '@http/transport'

export function useAddressesCacheService() {
  const queryCache = useQueryCache()
  const { list } = useAddressesQueryOptions()

  function invalidateAddressList() {
    return queryCache.invalidateQueries({ key: list.key })
  }
  function invalidateAll() {
    return queryCache.invalidateQueries()
  }
  function setAddressList(addresses: Address[]) {
    return queryCache.setQueryData(list.key, addresses)
  }

  return { invalidateAddressList, invalidateAll, setAddressList }
}
```
```ts {all|4|6|7|9-11}
import { useAddressesCacheService } from '@serverState/address'
import type { Address } from '@http/transport'

const addressesCache = useAddressesCacheService()

await addressesCache.invalidateAddressList()
await addressesCache.invalidateAll()

function updateAddressList(addresses: Address[]) {
  addressesCache.setAddressList(addresses)
}
```
````

</StoreCodePanel>
</div>

<blockquote data-node="cache-quote" class="absolute top-[716px] left-[28px] box-border m-0 flex w-[486px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] font-body text-[32px] leading-[1.2] text-secondary">
  <p class="m-0 w-full">«В программировании есть только две проблемы: инвалидация кеша и выбор имён переменных»</p>
</blockquote>
<!-- ARCHITECTURE-CODE-64:END -->


---
layout: store-code
---

<!-- TELEGRAM-ARTIFACT-65:START -->

<p data-node="artifact-kicker" class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Артефакт</p>

<h1 data-node="artifact-title" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-accent">Server State Layer Skill</h1>

<ul data-node="artifact-contents" class="absolute top-[320px] left-[28px] m-0 flex w-[836px] list-none flex-col gap-[32px] p-0 font-body font-normal text-[40px] leading-[1.2] text-white">
  <li class="flex items-baseline gap-[24px]"><span class="shrink-0" aria-hidden="true">•</span><span>Архитектурный слой</span></li>
  <li class="flex items-baseline gap-[24px]"><span class="shrink-0" aria-hidden="true">•</span><span>Инструкции по разработке</span></li>
  <li class="flex items-baseline gap-[24px]"><span class="shrink-0" aria-hidden="true">•</span><span>Лучшие практики и ограничения</span></li>
</ul>

<PublicImage data-node="telegram-channel-badge" class="absolute top-[272px] left-[978px] block h-[672px] w-[672px] max-w-none object-contain" src="/images/telegram-channel-badge.png" alt="Круглый чёрно-золотой значок: «Ну теперь заживём»" width="1254" height="1254" />

<!-- TELEGRAM-ARTIFACT-65:END -->


---
layout: store-code
---

<!-- CONCLUSIONS-66:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="1:2063" class="absolute top-[280px] left-[28px] m-0 w-[1704px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-transparent bg-clip-text bg-[linear-gradient(110.65609704351242deg,#fff_1.5437%,#999_99.362%)]">
  <span class="block">Есть такой тип</span>
  <span class="block text-accent">Server State</span>
</h1>

<p data-node="1:2064" class="absolute top-[528px] left-[28px] m-0 w-[1270px] font-body font-bold text-[48px] leading-[53px] tracking-[-2px] text-secondary">Server State – проекция серверного состояния на клиенте. Она может устареть и не является источником истины.</p>
<!-- CONCLUSIONS-66:END -->


---
layout: store-code
---

<!-- CONCLUSIONS-67:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="1:2072" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.95318947401859deg,#fff_1.5437%,#999_99.362%)]">Server State – это кеш</h1>

<div class="cache-conclusion-cards absolute top-[336px] left-[28px] grid w-[1704px] grid-cols-3 gap-[32px] font-body leading-[1.2] text-white">
  <div data-node="1:2073" class="box-border flex h-[456px] min-w-0 flex-col gap-[32px] rounded-[24px] border-2 border-solid border-white bg-white/5 px-[32px] pt-[40px] pb-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 font-bold text-[40px] text-white">Проекция</p>
    <p class="m-0 font-normal text-[32px] text-white">На клиенте хранится копия серверных данных, а не источник истины</p>
  </div>
  <div data-node="1:2076" class="box-border flex h-[456px] min-w-0 flex-col gap-[32px] rounded-[24px] border-2 border-solid border-white bg-white/5 px-[32px] pt-[40px] pb-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 font-bold text-[40px] text-white">Устаревает</p>
    <p class="m-0 font-normal text-[32px] text-white">Со временем локальная копия перестаёт соответствовать серверу</p>
  </div>
  <div data-node="1:2079" class="box-border flex h-[456px] min-w-0 flex-col gap-[32px] rounded-[24px] border-2 border-solid border-white bg-white/5 px-[32px] pt-[40px] pb-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 font-bold text-[40px] text-white">Обновляется</p>
    <p class="m-0 font-normal text-[32px] text-white">Свежая версия снова загружается из источника истины</p>
  </div>
</div>
<!-- CONCLUSIONS-67:END -->


---
layout: store-code
---

<!-- CONCLUSIONS-68:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="1:2089" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.58544816830903deg,#fff_1.5437%,#999_99.362%)]">Реализация Server State</h1>

<div class="client-cache-solutions absolute top-[304px] inset-x-[28px] flex justify-between gap-[32px] font-body">
  <div data-node="1:1433" class="cache-solution-card relative box-border h-[600px] w-[836px] shrink-0 rounded-[24px] border-2 border-solid border-[#41e786] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <div class="absolute top-[38px] left-[38px] flex h-[96px] w-[756px] items-center">
      <PublicImage src="/images/tanstack-query-logo.svg" class="block max-w-none" alt="TanStack" width="600" height="93.362" />
    </div>
    <div class="absolute top-[166px] left-[38px] flex h-[320px] w-[756px] items-center gap-[24px]">
      <p class="m-0 w-[412px] shrink-0 font-normal text-[32px] leading-[1.2] text-secondary">Query cache, keys, stale и gc timers, mutations, invalidation, refetch.</p>
      <a href="https://tanstack.com/query/latest" target="_blank" rel="noopener noreferrer" class="block h-[320px] w-[320px] shrink-0" aria-label="Документация TanStack Query">
        <PublicImage data-node="1:1447" src="/images/tanstack-query-qr-2x.png" class="block h-[320px] w-[320px] max-w-none" alt="QR-код документации TanStack Query" width="640" height="640" />
      </a>
    </div>
    <a href="https://tanstack.com/query/latest" target="_blank" rel="noopener noreferrer" class="absolute top-[518px] left-[38px] w-[756px] font-bold text-[24px] leading-[1.2] text-[#41e786] no-underline">tanstack.com/query</a>
  </div>
  <div data-node="1:1453" class="cache-solution-card relative box-border h-[600px] w-[836px] shrink-0 rounded-[24px] border-2 border-solid border-[#e4bd83] bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <div class="absolute top-[38px] left-[38px] flex h-[96px] w-[756px] items-center gap-[24px]">
      <PublicImage src="/images/pinia-colada-logo.svg" class="block max-w-none" alt="" aria-hidden="true" width="64" height="71.84" />
      <p class="m-0 w-[668px] font-bold text-[40px] leading-[1.2] text-white">Pinia Colada</p>
    </div>
    <div class="absolute top-[166px] left-[38px] flex h-[320px] w-[756px] items-center gap-[24px]">
      <p class="m-0 w-[412px] shrink-0 font-normal text-[32px] leading-[1.2] text-secondary">Та же модель Server State в экосистеме Vue: queries, mutations и cache entries.</p>
      <a href="https://pinia-colada.esm.dev/" target="_blank" rel="noopener noreferrer" class="block h-[320px] w-[320px] shrink-0" aria-label="Документация Pinia Colada">
        <PublicImage data-node="1:1500" src="/images/pinia-colada-qr-2x.png" class="block h-[320px] w-[320px] max-w-none" alt="QR-код документации Pinia Colada" width="640" height="640" />
      </a>
    </div>
    <a href="https://pinia-colada.esm.dev/" target="_blank" rel="noopener noreferrer" class="absolute top-[518px] left-[38px] w-[756px] font-bold text-[24px] leading-[1.2] text-[#e4bd83] no-underline">pinia-colada.esm.dev</a>
  </div>
</div>
<!-- CONCLUSIONS-68:END -->


---
layout: store-code
---

<!-- CONCLUSIONS-69:START -->
<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="1:2103" class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.27209169199533deg,#fff_1.5437%,#999_99.362%)]">Архитектурный слой</h1>

<p data-node="1:2104" class="absolute top-[280px] left-[28px] m-0 w-[1704px] font-body font-normal text-[40px] leading-[1.2] text-secondary">Чтобы контролировать кеш, ключи и инвалидации, ограничиваем работу с Server State архитектурным слоем.</p>

<div data-node="1:2105" class="absolute top-[456px] left-[28px] flex w-[1704px] flex-col gap-[24px] font-body">
  <div data-node="1:2106" class="box-border flex h-[128px] w-full shrink-0 items-center gap-[32px] rounded-[24px] border-2 border-solid border-[#a7b9f4] bg-white/5 px-[32px] py-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 w-[772px] shrink-0 font-bold text-[48px] leading-[53px] tracking-[-2px] text-[#a7b9f4]">Query Options</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[40px] leading-[1.2] text-secondary">Конфигурация запросов</p>
  </div>
  <div data-node="1:2109" class="box-border flex h-[128px] w-full shrink-0 items-center gap-[32px] rounded-[24px] border-2 border-solid border-[#e4bd83] bg-white/5 px-[32px] py-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 w-[772px] shrink-0 font-bold text-[48px] leading-[53px] tracking-[-2px] text-[#e4bd83]">Mutation Options</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[40px] leading-[1.2] text-secondary">Конфигурация мутаций</p>
  </div>
  <div data-node="1:2112" class="box-border flex h-[128px] w-full shrink-0 items-center gap-[32px] rounded-[24px] border-2 border-solid border-[#86caa9] bg-white/5 px-[32px] py-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
    <p class="m-0 w-[772px] shrink-0 font-bold text-[48px] leading-[53px] tracking-[-2px] text-[#86caa9]">Cache Service</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[40px] leading-[1.2] text-secondary">Сервис управления кешом</p>
  </div>
</div>
<!-- CONCLUSIONS-69:END -->


---
layout: store-code
variant: closing
---

<!-- CONCLUSIONS-70:START -->

<PublicImage data-node="1:2120" class="absolute top-[20px] left-[820px] block h-[1100px] w-[1100px] max-w-none object-contain opacity-75 pointer-events-none" src="/images/closing-glass-gears.png" alt="" aria-hidden="true" />

<h1 data-node="1:2123" class="absolute top-[220px] left-[28px] m-0 font-heading font-black text-[120px] leading-none tracking-[-2.4px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(99.61359467739067deg,#fff_1.5437%,#999_99.362%)]">Спасибо!</h1>

<a data-node="telegram-final-link" class="absolute top-[456px] left-[28px] block h-[320px] w-[320px] overflow-hidden rounded-[24px] bg-white" href="https://t.me/+g25E4B-9SscxOGM6" target="_blank" rel="noopener noreferrer" aria-label="Telegram: https://t.me/+g25E4B-9SscxOGM6">
  <PublicImage data-node="telegram-final-qr" class="block max-w-none" src="/images/telegram-final-qr.svg" alt="QR-код Telegram: https://t.me/+g25E4B-9SscxOGM6" width="320" height="320" />
</a>

<p data-node="1:2121" class="absolute top-[814px] left-[28px] m-0 w-[836px] font-body font-bold text-[40px] leading-[1.2] text-white">Telegram-канал</p>

<p data-node="1:2122" class="absolute top-[872px] left-[28px] m-0 w-[836px] font-body font-normal text-[24px] leading-[1.35] text-secondary">Больше про Server State и архитектуру фронтенда</p>
<!-- CONCLUSIONS-70:END -->
