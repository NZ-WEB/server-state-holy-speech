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

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

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

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[50px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(115.04475892308335deg,#fff_1.5437%,#999_99.362%)]">За что мы любим Store</h1>

<StoreBenefitsCards class="absolute inset-x-0 top-[210px]" />

---
layout: default
showStars: false
variant: none
showLogo: false
showNumbers: false
---

::canvas::

<PublicImage class="store-everything-background pointer-events-none absolute left-[-80px] top-0 block h-[1080px] w-[1920px] max-w-none" src="/images/store-everything-meme-background-2x.png" alt="" aria-hidden="true" />

<h1 class="absolute left-[249px] top-[88px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Давайте делать всё в Store!</h1>

<PublicImage class="store-everything-meme absolute left-[462px] top-[232px] block h-[751px] w-[836px] max-w-none object-cover" src="/images/store-everything-meme-2x.png" alt="Вовка в короне рядом с бочкой с надписью STORE" />

---
layout: default
variant: store-left
clicks: 4
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.1760574395592deg,#fff_1.5437%,#999_99.362%)]">Список адресов</h1>

<div class="store-addresses-content absolute left-[28px] right-0 top-[212px] flex items-start justify-between gap-[60px]">

<DeckStarList class="store-notes relative left-[-28px] w-[402px] shrink-0" variant="notes" :items="['addresses – данные', 'isLoading – загрузка', 'error – ошибка загрузки', 'loadAddresses – action']" />

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
layout: default
variant: store-left
clicks: 1
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(102.9576450088695deg,#fff_1.5437%,#999_99.362%)]">Все actions</h1>

<div class="store-actions-content absolute left-[28px] right-0 top-[212px] flex items-start justify-between gap-[60px]">

<DeckStarList class="store-notes relative left-[-28px] w-[402px] shrink-0" variant="notes" :items="['Добавить адрес', 'Удалить адрес', 'Обновить адрес']" />

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
layout: default
variant: store-left
clicks: 3
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.51865950802929deg,#fff_1.5437%,#999_99.362%)]">Активный адрес</h1>

<div class="store-active-address-content absolute left-[28px] right-0 top-[212px] flex items-start justify-between gap-[36px]">
<DeckStarList class="store-active-address-notes relative left-[-28px] w-[460px] shrink-0" variant="notes" :items="['activeAddressId – выбранный ID', 'activeAddress – активный адрес', 'selectAddress – action выбора']" />

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
layout: default
variant: store-left
clicks: 7
---


<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.0792614279172deg,#fff_1.5437%,#999_99.362%)]">Ближайший магазин</h1>

<div class="store-nearest-shop-body absolute left-[28px] right-0 top-[212px] flex items-start justify-between gap-[60px]">
<DeckStarList class="store-nearest-shop-notes relative left-[-28px] top-[-28px] w-[402px] shrink-0" variant="notes" :items="['store – найденный магазин', 'isLoading – загрузка', 'error – ошибка загрузки']" />

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
layout: default
variant: risk-left
---

<p class="invalidation-kicker absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent whitespace-nowrap">Реальная жизнь</p>

<h1 class="absolute top-[58px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(115.33539188446608deg,#fff_1.5437%,#999_99.362%)]">Контроль инвалидации</h1>

<div class="invalidation-clown-crop absolute left-[887px] top-[170px] w-[729px] h-[836px] overflow-hidden rounded-[26.954px] pointer-events-none">
  <PublicImage class="invalidation-clown absolute left-[-37.3327441%] top-[-5.8117626%] w-[174.6654726%] h-[105.8498564%] max-w-none" src="/images/invalidation-clown-personalized.png" alt="Автор доклада в костюме клоуна жонглирует мячами" />
</div>

<div class="invalidation-principles absolute left-0 top-[202px] flex w-[738px] flex-col items-start gap-[20px] font-body font-normal text-[32px] leading-[42px] text-body">
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
layout: default
variant: store-left
clicks: 3
---

<p class="absolute top-[8px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[58px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(99.34721910752687deg,#fff_1.5437%,#999_99.362%)]">Каталог</h1>

<div class="store-catalog-body absolute left-[28px] right-0 top-[184px] flex items-start justify-between gap-[60px]">
<DeckStarList class="store-catalog-notes relative left-[-28px] w-[402px] shrink-0" variant="notes" :items="['products – данные каталога', 'isLoading – загрузка', 'error – ошибка загрузки']" />

<StoreCodePanel :line-height="28">

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
      <p class="m-0 text-[32px] font-bold leading-[1.1] text-white">Неявные зависимости</p>
      <p class="m-0 text-[30px] leading-[38px] text-white/69">Необходимость писать велосипеды для соблюдения инварианта</p>
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
showStars: false
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

<h1 class="absolute top-[138px] left-[-1px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.5581102367891deg,#fff_1.5437%,#999_99.362%)]">Это же кеш!</h1>

<DeckStarList class="projection-notes absolute top-[300px] left-[-1px] w-[836px]" :items="['Источник истины находится на сервере', 'На клиенте хранится только копия', 'Эта копия может устаревать']" />

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
layout: default
variant: none
showLogo: false
showNumbers: false
---

<!-- FIGMA-95-4829:START -->
<ServerStateCookingIntro />
<!-- FIGMA-95-4829:END -->

---
layout: default
showStars: false
variant: none
showLogo: false
showNumbers: false
---

::canvas::

<PublicImage class="requirements-background pointer-events-none absolute left-[-80px] top-0 block h-[1080px] w-[1920px] max-w-none" src="/images/requirements-meme-background-2x.png" alt="" aria-hidden="true" />

<h1 class="absolute left-[389px] top-[88px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Соберем требования</h1>

<PublicImage class="requirements-meme absolute left-[430px] top-[232px] block h-[720px] w-[898px] max-w-none rounded-[32px] object-cover" src="/images/requirements-meme-2x.png" alt="Спанч Боб разводит руками под радугой" />

---
layout: default
variant: none
clicks: 1
---

<FigmaSlideBackdrop />

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[50px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(106.39648337165877deg,#fff_1.5437%,#999_99.362%)]">Кеш – это кеш!</h1>

<QueryMutationCache class="absolute top-[210px] left-0" :stage="$clicks" />


---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(103.96470826850641deg,#fff_1.5437%,#999_99.362%)]">Ключи кеша</h1>

<CatalogKeyTree class="absolute top-[304px] left-[28px]" :stage="$clicks" />


---
layout: default
variant: diagonal-left
---

<FigmaSlideBackdrop />

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[50px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.35786726442096deg,#fff_1.5437%,#999_99.362%)]">Долой Boilerplate</h1>

<div class="absolute top-[210px] left-0 flex items-start gap-[32px]">
  <QueryCapabilitiesPanel kind="query" />
  <QueryCapabilitiesPanel kind="mutation" />
</div>


---
layout: default
variant: diagonal-left
clicks: 4
---

<FigmaSlideBackdrop />

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[50px] left-[-6px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.92873093740087deg,#fff_1.5437%,#999_99.362%)]">Реактивность</h1>

<p class="absolute top-[202px] left-[-2px] w-[792px] m-0 font-body font-normal text-[30px] leading-[38px] text-body">Каждый следующий query получает входные данные из предыдущего звена цепочки</p>

<QueryReactivityChain class="absolute top-[342px] left-0" :stage="$clicks" />


---
layout: default
variant: diagonal-left
clicks: 3
---

<FigmaSlideBackdrop />

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>

<h1 class="absolute top-[50px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(106.51307381726778deg,#fff_1.5437%,#999_99.362%)]">Дедупликация</h1>

<SharedQueryCacheDiagram class="absolute top-[210px] left-0" :stage="$clicks" />


---
layout: default
variant: none
clicks: 5
---

<FigmaSlideBackdrop :secondary-x="1114" />

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent whitespace-nowrap">Server State</p>

<h1 class="absolute top-[50px] left-[-6px] m-0 w-max font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.74101414327697deg,#fff_1.5437%,#999_99.362%)]">Что мы <span class="text-accent">хотим</span></h1>

<ServerStateRequirementCircles :stage="$clicks" />


---
layout: default
variant: none
---

<FigmaSlideBackdrop />

<p data-node-id="89:3465" class="absolute left-[-1px] top-0 m-0 font-body text-[24px] font-bold leading-[1.1] text-accent">Server State</p>

<h1 data-node-id="89:3467" class="absolute left-[-6px] top-[50px] m-0 whitespace-nowrap bg-[linear-gradient(111.07667407611406deg,#fff_1.5437%,#999_99.362%)] bg-clip-text font-heading text-[80px] font-black leading-[0.9] tracking-[-1.6px] text-transparent">Решения уже есть!</h1>

<ServerStateSolutions class="absolute left-0 top-[210px]" />


---
layout: default
showStars: false
variant: none
showLogo: false
showNumbers: false
---

<RefactorIntro />


---
layout: default
variant: store-left
clicks: 4
---

<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[50px] left-[-5px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.95433580916409deg,#fff_1.5437%,#999_99.362%)]">Получение адресов</h1>

<div class="refactor-addresses-body absolute inset-x-0 top-[210px] flex items-start justify-between gap-[10px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
  <DeckStarList data-node="refactor-addresses-notes" class="w-[570px] shrink-0" style="--deck-list-font-size: 28px" :items="['query key для ключей', 'API fetcher для транспорта', 'staleTime - время свежести']" />

<StoreCodePanel class="!w-[1180px] !flex-none" data-node="refactor-addresses-code" :font-size="25" :line-height="26">

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
```ts {all|10|11|12}
import { useQuery } from '@pinia/colada'
import { addressesApi } from '@http/transport'

const {
  data: addresses,
  isLoading,
  error,
  refetch,
} = useQuery({
  key: ['addresses'],
  query: addressesApi.list,
  staleTime: 5 * MINUTE,
})
```
````

</StoreCodePanel>
</div>


---
layout: default
variant: none
---

<FigmaSlideBackdrop :focal-x="650" />
<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Server State</p>
<h1 class="absolute top-[50px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(110.4115335624527deg,#fff_1.5437%,#999_99.362%)]">Всему своё место</h1>
<RefactorStateCards class="absolute left-0 top-[210px]" />



---
layout: store-code
clicks: 7
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.14359990942712deg,#fff_1.5437%,#999_99.362%)]">Получение магазина</h1>

<div data-node="refactor-shop" class="absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
<div class="w-[402px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
  <p class="m-0">Реактивная зависимость через динамический ключ</p>
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
standardInsets: true
clicks: 8
---

<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(112.54071791881543deg,#fff_1.5437%,#999_99.362%)]">Получение каталога</h1>

<div data-node="refactor-catalog" class="absolute inset-x-0 top-[282px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0">
<div class="w-[402px] shrink-0 font-body font-normal text-[32px] leading-[1.2] text-secondary">
  <p class="m-0">Реактивная зависимость через динамический ключ</p>
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
standardInsets: true
clicks: 3
---

<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.38043091915237deg,#fff_1.5437%,#999_99.362%)]">Удалим же адрес</h1>

<p data-node="remove-address-description" class="absolute top-[262px] left-0 m-0 w-[836px] font-body font-normal text-[32px] leading-[1.2] text-secondary">После удаления кеш адресов инвалидируется, и вся цепочка запросов перезагружается</p>

<StoreCodePanel data-node="remove-address-code" :font-size="24" :line-height="24" class="absolute top-[402px] left-0 !w-[800px] [&_pre_code]:block motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0">

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

<RefactorInvalidationFlow class="absolute top-[222px] left-[924px]" />


---
layout: default
variant: none
---

<FigmaSlideBackdrop :show-secondary="false" focal-src="/images/figma-90-3834-focal.svg" :focal-x="-635" :focal-y="415" :focal-width="1475" :focal-height="1290" />

<p data-node="90:3835" class="absolute top-0 left-[-2px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 data-node="90:3837" class="absolute top-[50px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.97614104983313deg,#fff_1.5437%,#999_99.362%)]">Да будет инвариант</h1>

<RefactorInvariant class="absolute left-0 top-[202px]" />



---
layout: default
variant: none
title: Активный query
clicks: 8
---

<FigmaSlideBackdrop />

<div class="absolute left-[-1px] top-0 text-[24px] font-bold leading-[1.1] text-[#ed0f00]">Server State</div>
<h1 data-node="90:3800" class="absolute left-0 top-[50px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.15316910001444deg,#fff_1.5437%,#999_99.362%)]">Активный query</h1>

<div class="absolute left-[-2px] top-[202px] w-[792px] font-body text-[30px] font-normal leading-[38px] text-white/90">Активный query – query, у которого сейчас<br>есть хотя бы один подписчик</div>

<ActiveQueryFlow :stage="$clicks" class="absolute left-0 top-[341.8px]" />



---
layout: store-code
standardInsets: true
clicks: 5
---

<!-- NEW-FIGMA-146-2082:START -->

<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Refactor</p>

<h1 class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-white">Результаты рефакторинга</h1>

<div class="summary-refactor-results absolute top-[270px] left-0 flex w-[1760px] flex-col gap-0 font-body leading-[1.2]" role="table">
  <div v-click="1" data-summary-row="1" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[864px] shrink-0 text-[40px] font-bold text-white" role="cell">Boilerplate – всё</p>
    <p class="m-0 translate-y-[2px] w-[864px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Загрузка, ошибки и повторный запрос уже описаны библиотекой</p>
  </div>
  <div v-click="2" data-summary-row="2" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 -translate-y-[2px] w-[864px] shrink-0 text-[40px] font-bold text-white" role="cell">Дедупликация из коробки</p>
    <p class="m-0 -translate-y-[0.5px] w-[864px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Одинаковые queries разделяют один запрос</p>
  </div>
  <div v-click="3" data-summary-row="3" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[864px] shrink-0 text-[40px] font-bold text-white" role="cell">Кеш – это кеш</p>
    <p class="m-0 translate-y-[0.5px] w-[864px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Ключи, свежесть и инвалидация имеют готовый API</p>
  </div>
  <div v-click="4" data-summary-row="4" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 translate-y-px w-[864px] shrink-0 text-[40px] font-bold text-white" role="cell">Больше возможностей</p>
    <p class="m-0 translate-y-[2px] w-[864px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Фоновые обновления и оптимистичные изменения</p>
  </div>
  <div v-click="5" data-summary-row="5" class="box-border flex h-[120px] shrink-0 items-center gap-[32px] border-b border-solid border-white/20 transition-opacity !duration-500 ease-out motion-reduce:!duration-0" role="row">
    <p class="m-0 -translate-y-px w-[864px] shrink-0 text-[40px] font-bold text-white" role="cell">Реактивная модель</p>
    <p class="m-0 w-[864px] shrink-0 text-[32px] font-normal text-secondary" role="cell">Query зависят друг от друга и автоматически ждут входные данные</p>
  </div>
</div>

<!-- NEW-FIGMA-146-2082:END -->


---
layout: default
variant: none
title: Ну теперь заживем?
kicker: Server State
---

<FigmaSlideBackdrop />

<div class="absolute left-[-1px] top-0 font-body text-[24px] font-bold leading-[1.1] text-[#ed0f00]">Server State</div>
<h1 class="absolute left-[-6px] top-[50px] m-0 whitespace-nowrap font-heading text-[80px] font-black leading-[0.9] tracking-[-1.6px] bg-[linear-gradient(112.7566460850044deg,#fff_1.5437%,#999_99.362%)] bg-clip-text text-transparent">Ну теперь заживем?</h1>

<RefactorHappyEnd />



---
layout: default
showStars: false
variant: none
showLogo: false
showNumbers: false
title: А минусы будут?
---

<RefactorDownsides />



---
layout: default
variant: none
showLogo: false
---

<div class="absolute left-[-80px] top-[-88px] z-[-1] w-[1920px] h-[1080px] overflow-hidden bg-[#101010]" aria-hidden="true">
  <PublicImage class="absolute left-[-650px] top-[-580px] block max-w-none" src="/images/figma-90-4161-weakness-secondary.svg" width="1300" height="1000" alt="" />
  <PublicImage class="absolute left-[650px] top-[280px] block max-w-none" src="/images/figma-90-4162-weakness-focal.svg" width="1600" height="1250" alt="" />
</div>

<div class="absolute left-[-1px] top-0 whitespace-nowrap text-[24px] leading-[1.1] font-body font-bold text-accent">Server State</div>
<h1 class="absolute left-[-3px] top-[50px] m-0 whitespace-nowrap text-[80px] leading-[0.9] tracking-[-1.6px] font-heading font-black text-transparent bg-clip-text" style="background-image: linear-gradient(108.92797627857493deg, #fff 1.5437%, #999 99.362%)">Слабые стороны</h1>
<ServerStateWeaknesses class="absolute left-[-3px] top-[218px]" />
<PublicImage class="absolute left-0 top-[888px] block max-w-none" src="/images/figma-90-4163-weakness-logo.svg" width="92" height="32" alt="MAGNIT TECH" />


---
layout: store-code
standardInsets: true
variant: none
showLogo: false
---

<!-- NEW-FIGMA-90-3977:START -->
<ProjectControlBackdrop class="left-[-80px] top-0 z-[-1]" />
<p data-node-id="90:3981" class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Боль проекта</p>
<h1 data-node-id="90:3984" class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.16491593163272deg,#fff_1.5437%,#999_99.362%)]">Контроль теряется</h1>
<ProjectControlDiagram class="left-[-108px] top-0" />
<PublicImage data-node-id="90:3982" class="absolute bottom-[72px] left-0 block max-w-none pointer-events-none" src="/images/figma-90-3977-logo.svg" alt="MAGNIT TECH" width="92" height="32.0606" />
<!-- NEW-FIGMA-90-3977:END -->


---
layout: default
clicks: 3
variant: store-left
showLogo: false
---

<div class="pointer-events-none absolute left-[-80px] top-[-88px] z-[-1] h-[1080px] w-[1920px] overflow-hidden bg-[#101010]" aria-hidden="true">
  <PublicImage class="absolute left-[-650px] top-[-580px] block max-w-none" src="/images/figma-90-4173-secondary.svg" width="1300" height="1000" alt="" />
  <PublicImage class="absolute left-[650px] top-[280px] block max-w-none" src="/images/figma-90-4173-focal.svg" width="1600" height="1250" alt="" />
</div>
<p class="absolute left-[-1px] top-0 m-0 font-body text-[24px] font-bold leading-[1.1] text-[#ed0f00]">Боль проекта</p>
<h1 class="absolute left-[-5px] top-[50px] m-0 whitespace-nowrap bg-clip-text font-heading text-[80px] font-black leading-[0.9] tracking-[-1.6px] text-transparent" style="background-image:linear-gradient(105.08129053889449deg,#fff 1.5437%,#999 99.362%)">Последствия</h1>
<ServerStateConsequences class="absolute left-0 top-[218px]" :stage="$clicks" />
<PublicImage class="absolute left-0 top-[888px] block max-w-none" src="/images/figma-90-4173-logo.svg" width="92" height="32" alt="MAGNIT TECH" />


---
layout: default
clicks: 4
variant: store-left
showLogo: false
---

<div class="pointer-events-none absolute left-[-80px] top-[-88px] z-[-1] h-[1080px] w-[1920px] overflow-hidden bg-[#101010]" aria-hidden="true">
  <PublicImage class="absolute left-[-650px] top-[-580px] block max-w-none" src="/images/figma-90-4173-secondary.svg" width="1300" height="1000" alt="" />
  <PublicImage class="absolute left-[650px] top-[280px] block max-w-none" src="/images/figma-90-4173-focal.svg" width="1600" height="1250" alt="" />
</div>
<p class="absolute left-[-1px] top-0 m-0 font-body text-[24px] font-bold leading-[1.1] text-[#ed0f00]">Боль проекта</p>
<h1 class="absolute left-[-5px] top-[50px] m-0 whitespace-nowrap bg-clip-text font-heading text-[80px] font-black leading-[0.9] tracking-[-1.6px] text-transparent" style="background-image:linear-gradient(114.77364587733764deg,#fff 1.5437%,#999 99.362%)">Решаем архитектурой</h1>
<ArchitecturePrinciples class="absolute left-0 top-[218px]" :stage="$clicks" />
<PublicImage class="absolute left-0 top-[888px] block max-w-none" src="/images/figma-90-4173-logo.svg" width="92" height="32" alt="MAGNIT TECH" />


---
layout: default
variant: none
showLogo: false
clicks: 1
---

<!-- NEW-FIGMA-90-3777:START -->
<div class="absolute left-[-80px] top-[-88px] z-[-1] w-[1920px] h-[1080px] overflow-hidden bg-[#101010]" aria-hidden="true">
  <PublicImage class="absolute left-[-650px] top-[-580px] block max-w-none" src="/images/figma-deck-red-secondary.svg" width="1300" height="1000" alt="" />
</div>
<p data-node-id="90:3779" class="absolute left-[805px] top-0 m-0 font-body text-[24px] font-bold leading-[1.1] text-accent">Архитектура</p>
<h1 data-node-id="90:3781" class="absolute left-[465px] top-[50px] m-0 whitespace-nowrap font-heading text-[80px] font-black leading-[0.9] tracking-[-1.6px] text-transparent bg-clip-text bg-[linear-gradient(110.1661906828467deg,#fff_1.5437%,#999_99.362%)]">Server State Layer</h1>
<ExpandingServerStateLayer class="absolute left-0 top-[210px]" :stage="$clicks" />
<PublicImage data-node-id="90:3780" class="absolute left-0 top-[888px] block max-w-none" src="/images/figma-90-3780-layer-logo.svg" width="92" height="32" alt="MAGNIT TECH" />
<!-- NEW-FIGMA-90-3777:END -->


---
layout: store-code
standardInsets: true
clicks: 9
---

<!-- ARCHITECTURE-CODE-62:START -->
<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[138px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.76449780050385deg,#fff_1.5437%,#999_99.362%)]">Query Options</h1>

<div class="architecture-code-body absolute inset-x-0 top-[254px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <DeckStarList data-node="architecture-notes" class="w-[502px] shrink-0" style="margin-top: 28px; --deck-list-color: rgba(255, 255, 255, 0.8)" :items="['Все Query Options домена в одном месте', 'Скрываем реализацию', 'Декларативный интерфейс наружу']" />

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
standardInsets: true
clicks: 12
---

<!-- ARCHITECTURE-CODE-63:START -->
<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.85989467988094deg,#fff_1.5437%,#999_99.362%)]">Mutation Options</h1>

<div class="architecture-code-body absolute inset-x-0 top-[254px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <DeckStarList data-node="architecture-notes" class="w-[402px] shrink-0" style="margin-top: 28px; --deck-list-color: rgba(255, 255, 255, 0.8)" :items="['Операции записи домена – в одном месте', 'Скрываем реализацию', 'Декларативный интерфейс наружу']" />

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
standardInsets: true
clicks: 9
---

<!-- ARCHITECTURE-CODE-64:START -->
<p class="absolute top-[88px] left-0 m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Архитектура</p>

<h1 class="absolute top-[138px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.78797602456692deg,#fff_1.5437%,#999_99.362%)]">Cache Service</h1>

<div class="architecture-code-body absolute inset-x-0 top-[254px] flex items-start justify-between gap-[32px] motion-reduce:[&_.shiki-magic-move-item]:!duration-0 motion-reduce:[&_.shiki-magic-move-item]:!delay-0 motion-reduce:[&_.shiki-magic-move-container]:!duration-0 motion-reduce:[&_.shiki-magic-move-container]:!delay-0 motion-reduce:[&_pre_span]:!duration-0 motion-reduce:[&_pre_span]:!delay-0" :data-stage="$clicks">
  <DeckStarList data-node="architecture-notes" class="w-[402px] shrink-0" style="margin-top: 28px; --deck-list-color: rgba(255, 255, 255, 0.8)" :items="['Все операции с кешем домена в одном месте', 'Скрываем детали реализации', 'Декларативный интерфейс наружу']" />

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


<!-- ARCHITECTURE-CODE-64:END -->


---
layout: default
variant: none
showLogo: false
---

<ServerStateSkillsSlide />


---
layout: default
variant: none
showLogo: false
---

<ServerStateTypeIntro />


---
layout: default
variant: none
showLogo: false
---

<!-- CONCLUSIONS-67:START -->
<FigmaSlideBackdrop :focal-x="650" />

<p data-node="90:3754" class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="90:3756" class="absolute top-[50px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.95318947401859deg,#fff_1.5437%,#999_99.362%)]">Server State – это кэш</h1>

<ServerStateCacheConclusion class="absolute top-[210px] left-0" />

<PublicImage data-node="90:3755" class="absolute top-[888px] left-0 block max-w-none pointer-events-none" src="/images/figma-90-3751-logo.svg" width="92" height="32" alt="MAGNIT TECH" />
<!-- CONCLUSIONS-67:END -->


---
layout: default
variant: store-left
---

<!-- CONCLUSIONS-68:START -->
<p class="absolute top-0 left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Выводы</p>

<h1 data-node="1:2089" class="absolute top-[50px] left-0 m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.58544816830903deg,#fff_1.5437%,#999_99.362%)]">Реализация Server State</h1>

<ServerStateSolutions class="absolute top-[210px] left-0" />
<!-- CONCLUSIONS-68:END -->


---
layout: default
variant: none
showLogo: false
---

<!-- CONCLUSIONS-69:START -->
<ServerStateArchitectureConclusion />
<!-- CONCLUSIONS-69:END -->


---
layout: default
variant: none
showLogo: false
showNumbers: false
---

<!-- CONCLUSIONS-70:START -->
<ThanksSlide />
<!-- CONCLUSIONS-70:END -->
