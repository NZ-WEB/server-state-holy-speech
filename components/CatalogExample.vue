<script setup lang="ts">
import { useSlideContext } from '@slidev/client'
import { computed } from 'vue'

const props = withDefaults(defineProps<{ static?: boolean }>(), { static: false })
const { $clicks } = useSlideContext()
const stage = computed(() => props.static ? 4 : $clicks.value)
const products = [
  { id: 'lollipop', click: 1, name: 'Леденец “Петушок”', price: '250 ₽', image: '/images/catalog-lollipop-2x.png' },
  { id: 'biscuits', click: 2, name: 'Печенье Юбилейное', price: '64 ₽', image: '/images/catalog-biscuits-2x.png' },
  { id: 'coffee', click: 3, name: 'Кофе зерновой', price: '479 ₽', image: '/images/catalog-coffee-2x.png' },
] as const
</script>

<template>
  <section
    class="catalog-example box-border flex h-[629px] w-[1052px] flex-col gap-[32px] overflow-hidden rounded-[32px] border border-solid border-white/20 bg-white/5 bg-[linear-gradient(180deg,rgba(0,0,0,0.3)_0%,transparent_14%,transparent_86%,rgba(255,255,255,0.04)_100%)] p-[32px] font-body shadow-[inset_12px_0_24px_rgba(0,0,0,0.35),inset_-12px_0_24px_rgba(255,255,255,0.05)] backdrop-blur-[19px]"
    aria-label="Каталог магазина Магнит"
  >
    <div class="flex h-[118px] w-full shrink-0 flex-col gap-[16px]">
      <p class="m-0 text-[20px] leading-[24px] text-accent">Каталог</p>
      <div class="flex flex-col gap-[4px]">
        <h2 class="m-0 font-body text-[40px] font-bold leading-[1.2] text-white">Магнит</h2>
        <p
          class="catalog-delivery m-0 h-[26px] w-[457px] whitespace-nowrap text-[24px] leading-[1.35] text-secondary !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"
          :class="stage >= 4 ? 'opacity-100 translate-y-0' : 'opacity-0 pointer-events-none translate-y-[12px]'"
          :aria-hidden="stage < 4"
        >Адрес доставки: ул. Ленина, 10 · Москва</p>
      </div>
    </div>
    <div class="flex w-full items-start gap-[16px]">
      <article
        v-for="product in products"
        :key="product.id"
        :data-product="product.id"
        class="catalog-product box-border flex h-[413px] w-[318px] shrink-0 flex-col gap-[24px] rounded-[32px] border border-solid border-white/20 bg-[#252525] px-[8px] pb-[20px] pt-[8px] text-white !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"
        :class="stage >= product.click ? 'opacity-100 translate-y-0' : 'opacity-0 pointer-events-none translate-y-[48px]'"
        :aria-hidden="stage < product.click"
      >
        <img :src="product.image" :alt="product.name" class="block h-[287px] w-[300px] shrink-0 rounded-[24px] object-cover">
        <div class="box-border flex w-full flex-col gap-[2px] px-[16px]">
          <p class="m-0 h-[32px] w-full whitespace-nowrap text-[24px] leading-[1.35]">{{ product.name }}</p>
          <p class="m-0 w-full text-[30px] font-bold leading-[38px]">{{ product.price }}</p>
        </div>
      </article>
    </div>
  </section>
</template>
