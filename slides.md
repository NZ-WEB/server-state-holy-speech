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
  <PublicImage class="absolute left-[734px] top-[-170px] w-[1320px] h-[1320px] max-w-none object-cover opacity-75" src="/images/cover-glass-gears.png" alt="" aria-hidden="true" />
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
  <PublicImage class="absolute right-0 bottom-0 w-[935px] h-[1016px] max-w-none object-cover" src="/images/speaker-portrait.png" alt="Евгений Федосеев" />
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
    <PublicImage class="absolute left-[-100px] top-[-100px] max-w-none" :src="'/images/delete-address-focal.svg'" alt="" />
  </div>
</div>

---
layout: default
variant: cooking
---

<h1 class="absolute left-[-6px] top-[96px] m-0 w-[817px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.87524243018746deg,#fff_1.5437%,#999_99.362%)]">Как это готовить?</h1>

<p class="absolute left-[-2px] top-[200px] m-0 w-[1704px] font-body font-normal text-[32px] leading-[42px] text-accent"><span class="relative top-[1px]">Выглядит сложно даже без кода</span></p>

<PublicImage class="cooking-meme absolute left-[538px] top-[247px] w-[1260px] h-[834px] max-w-none object-cover" src="/images/cooking-meme.png" alt="Мужчина разводит руками в недоумении" />

<PublicImage class="cooking-glass absolute left-[404px] top-[475.745px] w-[553.578px] h-[232.192px] max-w-none origin-top-left rotate-[-8.177960676deg] opacity-85" src="/images/cooking-glass.png" alt="Я просто хотел удалить адрес" />

---
layout: default
variant: section-right
---

<PublicImage class="absolute left-[838px] top-[62px] w-[934px] h-[981px] max-w-none object-cover opacity-85 pointer-events-none" src="/images/state-types-intro-glass-controls.png" alt="" aria-hidden="true" />

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

---
layout: default
variant: diagonal-left
clicks: 4
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Local или Application</p>

<h1 class="absolute top-[146px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.1760574395592deg,#fff_1.5437%,#999_99.362%)]">Список адресов</h1>

<div class="real-case-bullets absolute top-[298px] left-[-1px] flex w-[554px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на сервере</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Меняется by action</span></p>
  <p v-click="3" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>От него зависит Application State</span></p>
  <p v-click="4" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется только в адресах</span></p>
</div>

<AddressExample static :active-address="null" class="absolute top-[308px] left-[804px]" />

---
layout: default
variant: diagonal-left
clicks: 3
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[146px] left-[0] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.51865950802929deg,#fff_1.5437%,#999_99.362%)]">Активный адрес</h1>

<div class="real-case-bullets absolute top-[298px] left-[-1px] flex w-[469px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на клиенте</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Меняется со временем</span></p>
  <p v-click="3" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется повсеместно</span></p>
</div>

<AddressExample static class="absolute top-[308px] left-[804px]" />

---
layout: default
variant: diagonal
clicks: 3
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Local или Application</p>

<h1 class="absolute top-[146px] left-[0] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(113.25069355919166deg,#fff_1.5437%,#999_99.362%)]">А каталог и магазин?</h1>

<div class="real-case-bullets absolute top-[298px] left-[-1px] flex w-[529px] flex-col gap-[20px] font-body text-[32px] leading-[42px] text-body">
  <p v-click="1" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Истина на сервере</span></p>
  <p v-click="2" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Зависит от выбранного адреса</span></p>
  <p v-click="3" class="m-0 flex whitespace-nowrap !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"><span class="w-[44px] shrink-0" aria-hidden="true">✦</span><span>Используется не везде</span></p>
</div>

<CatalogExample static class="absolute top-[308px] left-[708px]" />

---
layout: default
variant: diagonal
clicks: 4
---

<p class="absolute top-[96px] left-[-1px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Реализация</p>

<h1 class="absolute top-[146px] left-[-2px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(115.04475892308335deg,#fff_1.5437%,#999_99.362%)]">За что мы любим Store</h1>

<StoreBenefitsCards class="absolute inset-x-0 top-[298px]" />

---
layout: default
variant: none
showLogo: false
showNumbers: false
---

<PublicImage class="store-everything-background pointer-events-none absolute left-[-80px] top-0 block h-full w-[1920px] max-w-none" :src="'/images/store-everything-background-2x.png'" alt="" />

<div class="pointer-events-none absolute left-[-250.914px] top-[285.12px] flex h-[846.626px] w-[1154.261px] items-center justify-center" aria-hidden="true">
  <div class="relative h-[587.001px] w-[1033.32px] rotate-[-15.83deg]">
    <PublicImage class="absolute left-[-100px] top-[-100px] max-w-none" :src="'/images/delete-address-focal.svg'" alt="" />
  </div>
</div>

<PublicImage class="store-everything-character absolute left-[770.273px] top-[224px] block h-[735px] w-[496.274px] max-w-none" :src="'/images/store-everything-character-2x.png'" alt="Вовка из мультфильма «Вовка в Тридевятом царстве»" />

<PublicImage class="store-everything-bucket absolute left-[474px] top-[575.651px] block h-[383.129px] w-[316.617px] max-w-none" :src="'/images/store-everything-bucket-2x.png'" alt="Ведро с берёзовыми поленьями" />

<h1 class="absolute top-[88px] left-[249px] m-0 w-[1262px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-[#fafafa]">Давайте делать всё в Store!</h1>

---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Store-реализация</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(108.1760574395592deg,#fff_1.5437%,#999_99.362%)]">Список адресов</h1>

<div class="store-addresses-content absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">

<div class="store-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body text-[30px] leading-[38px] text-body">
  <p class="m-0"><span class="font-bold text-accent">addresses</span> – данные</p>
  <p class="m-0"><span class="font-bold text-accent">isLoading</span> – загрузка</p>
  <p class="m-0"><span class="font-bold text-accent">error</span> – ошибка</p>
  <p class="m-0"><span class="font-bold text-accent">loadAddresses</span> – action</p>
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

<div class="store-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body font-bold text-[30px] leading-[38px] text-accent">
  <p class="m-0">Добавить адрес</p>
  <p class="m-0">Удалить адрес</p>
  <p class="m-0">Обновить адрес</p>
</div>

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

<div class="store-active-address-content absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">
<div class="store-active-address-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body text-[30px] leading-[38px] text-body">
  <p class="m-0"><span class="font-bold text-accent">activeAddressId</span> – выбранный ID</p>
  <p class="m-0"><span class="font-bold text-accent">activeAddress</span> – вычисляемый адрес</p>
  <p class="m-0"><span class="font-bold text-accent">selectAddress</span> – action выбора</p>
</div>

<StoreCodePanel :line-height="28">

````md magic-move
```ts {6-7|9-12|15-17|19}
import { defineStore } from 'pinia'
import { computed, ref } from 'vue'
import { useAddressesStore } from './addresses'

export const useActiveAddressStore = defineStore('active-address', () => {
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

<div class="refresh-conditions absolute top-[496px] inset-x-[28px] flex flex-col gap-[16px] font-body">
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
<div class="store-nearest-shop-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body text-[32px] leading-[1.2] text-white">
  <p class="m-0"><span class="font-bold text-accent">store</span> – найденный магазин</p>
  <p class="m-0"><span class="font-bold text-accent">isLoading</span> – загрузка</p>
  <p class="m-0"><span class="font-bold text-accent">error</span> – ошибка</p>
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
  <PublicImage class="invalidation-clown absolute left-[-37.3327441%] top-[-5.8117626%] w-[174.6654726%] h-[105.8498564%] max-w-none" src="/images/invalidation-clown.png" alt="Клоун жонглирует мячами" />
</div>

<div class="invalidation-principles absolute left-[28px] top-[300px] flex flex-col items-start gap-[32px] font-body text-[32px] leading-[42px] text-white">
  <div class="invalidation-principle flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/invalidation-cross.svg" alt="" width="64" height="64" />
    <p class="m-0 whitespace-nowrap">Ручное поддержание инвариантов</p>
  </div>
  <div class="invalidation-principle flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/invalidation-cross.svg" alt="" width="64" height="64" />
    <p class="m-0 whitespace-nowrap">Разрозненная логика зависимостей</p>
  </div>
  <div class="invalidation-principle flex items-center gap-[32px]">
    <PublicImage class="block shrink-0 max-w-none" src="/images/invalidation-cross.svg" alt="" width="64" height="64" />
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
---


<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(109.33529736428274deg,#fff_1.5437%,#999_99.362%)]">Проблемы watch</h1>

<div class="watch-problems absolute top-[304px] inset-x-[28px] flex flex-col gap-[24px] font-body">
  <div class="watch-problem relative flex h-[176px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">01</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[12px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Race conditions</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Старый ответ может прийти позже и перезаписать актуальные данные.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div class="watch-problem relative flex h-[176px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">02</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[12px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Неявность</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Причина запроса спрятана в цепочке реактивных наблюдателей.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
  <div class="watch-problem relative flex h-[176px] items-center gap-[48px]">
    <p class="m-0 w-[168px] shrink-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] text-accent">03</p>
    <div class="min-w-0 flex-1 flex flex-col gap-[12px] leading-[1.2]">
      <p class="m-0 font-bold text-[40px] text-white">Отмена запросов</p>
      <p class="m-0 font-normal text-[32px] text-secondary">Очистку таймеров и отмену устаревших запросов пишем вручную.</p>
    </div>
    <div class="absolute bottom-0 inset-x-0 h-px bg-white/20" aria-hidden="true"></div>
  </div>
</div>


---
layout: store-code
---


<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(102.13636440638527deg,#fff_1.5437%,#999_99.362%)]">Boilerplate</h1>

<ul class="boilerplate-list absolute top-[320px] left-[28px] m-0 p-0 w-[836px] list-none flex flex-col gap-[32px] font-body font-normal text-[40px] leading-[1.2] text-white">
  <li class="flex items-center gap-[24px]"><span class="w-[8px] h-[8px] shrink-0 bg-accent" aria-hidden="true"></span><span class="min-w-0 flex-1">Одинаковые CRUD-ы</span></li>
  <li class="flex items-center gap-[24px]"><span class="w-[8px] h-[8px] shrink-0 bg-accent" aria-hidden="true"></span><span class="min-w-0 flex-1">Флаги асинхронщины</span></li>
  <li class="flex items-center gap-[24px]"><span class="w-[8px] h-[8px] shrink-0 bg-accent" aria-hidden="true"></span><span class="min-w-0 flex-1">Обработка ошибок</span></li>
  <li class="flex items-center gap-[24px]"><span class="w-[8px] h-[8px] shrink-0 bg-accent" aria-hidden="true"></span><span class="min-w-0 flex-1">Загрузка из API</span></li>
</ul>

<PublicImage class="boilerplate-iceberg absolute top-[288px] right-[27.56px] block max-w-none w-[584.878px] h-[640px] rounded-[16px] object-cover" :src="'/images/boilerplate-iceberg-2x.png'" alt="Айсберг: над водой data, под водой isLoading, error, refetch, fetch, clear" width="1170" height="1280" />

---
layout: store-code
clicks: 1
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Альтернатива Store</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(112.97189370889106deg,#fff_1.5437%,#999_99.362%)]">Спасибо composable</h1>

<div class="composable-body absolute inset-x-[28px] top-[300px] flex items-start justify-between gap-[32px]">
  <div class="composable-notes flex w-[402px] shrink-0 flex-col gap-[24px] font-body font-normal text-[32px] leading-[1.2] text-white">
    <p class="m-0">Реализует boilerplate</p>
    <p class="m-0">Скрывает реализацию</p>
  </div>

<StoreCodePanel :line-height="28" class="relative top-[-28px]">

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
layout: store-code
variant: none
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы composable</p>

<h1 class="absolute top-[156px] left-[28px] m-0 w-[1122px] font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-white">Дедупликация запросов</h1>

<RequestDeduplicationDiagram />

---
layout: store-code
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Проблемы composable</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(116.7271941937475deg,#fff_1.5437%,#999_99.362%)]">Composable не подходит</h1>

<div class="composable-limitations absolute top-[375px] inset-x-[28px] flex flex-col gap-[64px] font-body">
  <div class="composable-limitations-row flex items-start gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">Нет дедупликации</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[42px] text-secondary">Одинаковые запросы запускаются повторно в разных компонентах</p>
  </div>
  <div class="composable-limitations-separator h-px shrink-0 bg-white/20" aria-hidden="true"></div>
  <div class="composable-limitations-row flex items-start gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">Дублирование состояния</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[42px] text-secondary">Каждый экземпляр composable хранит собственные данные, загрузку и ошибку</p>
  </div>
  <div class="composable-limitations-separator h-px shrink-0 bg-white/20" aria-hidden="true"></div>
  <div class="composable-limitations-row flex items-start gap-[32px]">
    <p class="m-0 w-[402px] shrink-0 font-bold text-[40px] leading-[1.2] text-white">Сложный refresh</p>
    <p class="m-0 min-w-0 flex-1 font-normal text-[32px] leading-[42px] text-secondary">Интервалы и повторные запросы приходится координировать вручную</p>
  </div>
</div>

---
layout: store-code
clicks: 3
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Кэш</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(111.40703837884945deg,#fff_1.5437%,#999_99.362%)]">Кэш – что за зверь?</h1>

<p class="absolute top-[300px] left-[28px] w-[836px] m-0 font-body font-normal text-[32px] leading-[42px] text-white">Кэш – временная копия данных, которая позволяет не обращаться к источнику истины при каждом чтении.</p>

<p class="absolute top-[466px] left-[28px] w-[704px] m-0 font-body font-normal text-[24px] leading-[1.35] text-secondary">Ключ кэша – уникальный идентификатор, по которому находим нужную копию данных.</p>

<BackendCacheDiagram class="absolute top-[304px] left-[896px]" />

---
layout: store-code
clicks: 4
---

<p class="absolute top-[108px] left-[28px] m-0 font-body font-bold text-[24px] leading-[1.1] text-accent">Кэш</p>

<h1 class="absolute top-[156px] left-[28px] m-0 font-heading font-black text-[80px] leading-[0.9] tracking-[-1.6px] whitespace-nowrap text-transparent bg-clip-text bg-[linear-gradient(105.38811141368086deg,#fff_1.5437%,#999_99.362%)]">Инвалидация</h1>

<p class="invalidation-definition absolute top-[300px] left-[28px] m-0 w-[1268px] font-body font-normal text-[32px] leading-[42px] text-secondary">Инвалидация кэша – пометка сохранённых данных как устаревших, после которой следующий потребитель получает свежую версию.</p>

<InvalidationFlow class="absolute top-[574px] left-[28px]" :stage="$clicks" />
