<script setup lang="ts">
import { useSlideContext } from '@slidev/client'
import AddressExampleRow from './AddressExampleRow.vue'

const { $clicks } = useSlideContext()
const addresses = [
  { id: 'home', label: 'ДОМ', street: 'ул. Ленина, 10 · Москва', details: 'Подъезд 2, этаж 7, кв. 48' },
  { id: 'work', label: 'РАБОТА', street: 'ул. Тверская, 12 · Москва', details: 'Бизнес-центр «Центральный», вход со\u00a0двора' },
  { id: 'parents', label: 'РОДИТЕЛИ', street: 'пр-т Победы, 4 · Химки', details: 'Подъезд 1, этаж 2, кв. 13' },
] as const
</script>

<template>
  <section
    class="address-example box-border flex w-[836px] flex-col gap-[24px] overflow-hidden rounded-[32px] border border-solid border-white/20 bg-white/5 bg-[linear-gradient(180deg,rgba(0,0,0,0.3)_0%,transparent_14%,transparent_86%,rgba(255,255,255,0.04)_100%)] p-[32px] font-body shadow-[inset_12px_0_24px_rgba(0,0,0,0.35),inset_-12px_0_24px_rgba(255,255,255,0.05)] backdrop-blur-[19px] !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"
    :class="$clicks >= 1 ? 'opacity-100 translate-x-0' : 'opacity-0 pointer-events-none translate-x-[12px]'"
    aria-label="Пример списка адресов"
  >
    <div class="flex h-[52px] w-full shrink-0 items-center justify-between overflow-hidden">
      <h2 class="m-0 font-body text-[40px] font-bold leading-[1.2] text-white">Мои адреса</h2>
      <button
        type="button"
        :tabindex="$clicks >= 2 ? 0 : -1"
        class="flex h-[52px] shrink-0 items-center justify-center gap-[8px] overflow-hidden rounded-[48px] border-0 bg-[#cf1e12] py-[12px] pl-[16px] pr-[24px] font-body text-[24px] font-bold leading-[1.1] text-white !transition-[opacity,transform] !duration-500 ease-out motion-reduce:!duration-0 motion-reduce:!transform-none"
        :class="$clicks >= 2 ? 'opacity-100 translate-y-0' : 'opacity-0 pointer-events-none translate-y-[8px]'"
      >
        <span class="relative block h-[28px] w-[28px] shrink-0 overflow-hidden" aria-hidden="true">
          <img class="absolute left-[4.8333px] top-[4.8333px] block max-w-none" src="/images/addresses-plus.svg" alt="">
        </span>
        <span class="whitespace-nowrap">Добавить адрес</span>
      </button>
    </div>
    <div class="flex w-full flex-col gap-[16px]">
      <AddressExampleRow
        v-for="address in addresses"
        :key="address.id"
        :label="address.label"
        :street="address.street"
        :details="address.details"
        :active="address.id === 'home' && $clicks >= 4"
        :show-delete="$clicks >= 3"
      />
    </div>
  </section>
</template>
