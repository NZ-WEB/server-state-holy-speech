<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps<{ stage: number }>()
const expanded = computed(() => props.stage >= 1)

const capabilities = [
  { nodeId: '1:1894', title: 'Query Options', description: 'конфигурация запросов' },
  { nodeId: '1:1897', title: 'Mutation Options', description: 'конфигурация мутаций' },
  { nodeId: '1:1900', title: 'Cache Service', description: 'управление кешом' },
] as const
</script>

<template>
  <div data-node-id="1:1882" class="expanding-server-state-layer relative h-[552px] w-[1704px] font-body text-white" role="group" aria-label="API, Server State Layer, UI" :data-expanded="expanded">
    <div data-node="api" data-node-id="1:1890" class="absolute left-0 top-[200px] box-border flex h-[160px] w-[402px] items-center justify-center rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
      <p class="m-0 text-center text-[32px] font-bold leading-[1.2]">API</p>
    </div>

    <section
      data-node="server-state-layer"
      data-node-id="1:1892"
      class="absolute left-[434px] box-border w-[836px] overflow-hidden rounded-[24px] border-2 border-solid border-accent bg-white/5 backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)] transition-[height,top] duration-700 ease-in-out motion-reduce:duration-0"
      :class="expanded ? 'top-0 h-[552px]' : 'top-[200px] h-[160px]'"
    >
      <h2 data-node-id="1:1893" class="absolute left-[30px] m-0 w-[772px] text-center text-[40px] font-bold leading-[48px] transition-[top] duration-700 ease-in-out motion-reduce:duration-0" :class="expanded ? 'top-[30px]' : 'top-[54px]'">Server State Layer</h2>

      <div
        data-node="layer-capabilities"
        class="absolute left-[30px] top-[94px] flex w-[772px] flex-col gap-[16px] transition-[opacity,transform] duration-500 ease-out motion-reduce:duration-0 motion-reduce:delay-0"
        :class="expanded ? 'opacity-100 translate-y-0 delay-200' : 'opacity-0 translate-y-[16px] delay-0'"
        :aria-hidden="!expanded"
      >
        <article v-for="capability in capabilities" :key="capability.title" :data-node-id="capability.nodeId" :data-capability="capability.title" class="box-border flex h-[128px] w-full flex-col items-center justify-center gap-[4px] rounded-[24px] border border-solid border-white/20 bg-white/5 px-[24px] py-[12px] text-center text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
          <p class="m-0 w-full font-bold">{{ capability.title }}</p>
          <p class="m-0 w-full font-normal text-secondary">{{ capability.description }}</p>
        </article>
      </div>
    </section>

    <div data-node="ui" data-node-id="1:1903" class="absolute right-0 top-[200px] box-border flex h-[160px] w-[402px] flex-col items-center justify-center gap-[16px] rounded-[24px] border border-solid border-white/20 bg-white/5 p-[24px] text-center text-[32px] leading-[1.2] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]">
      <p class="m-0 w-full font-bold">UI</p>
      <p class="m-0 w-full font-normal text-secondary">компоненты</p>
    </div>

    <PublicImage class="absolute left-[-108px] top-[-304px] pointer-events-none max-w-none" src="/images/server-state-layer-api.svg" width="1920" height="1080" alt="" />
    <PublicImage class="absolute left-[-108px] top-[-304px] pointer-events-none max-w-none" src="/images/server-state-layer-ui.svg" width="1920" height="1080" alt="" />
  </div>
</template>
