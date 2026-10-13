<script setup lang="ts">
const props = defineProps<{ stage: number }>()

function revealClass(step: number) {
  return props.stage >= step ? 'opacity-100' : 'opacity-0'
}

// Positions retain the 1920 × 1080 Figma geometry within SlideFrame's 80px gutter.
const regions = [
  { title: 'Backend', stage: 1, position: 'left-[28px] w-[402px]' },
  { title: 'Frontend', stage: 2, position: 'left-[462px] w-[1270px]' },
] as const

const nodes = [
  { key: 'addresses', stage: 3, title: 'Адреса', description: 'True State', position: 'left-[52px] top-[444px] w-[354px] h-[160px]', border: 'border-[#7f9fff]' },
  { key: 'api', stage: 4, title: 'API', description: '', position: 'left-[52px] top-[700px] w-[354px] h-[96px]', border: 'border-[#7f9fff]' },
  { key: 'list', stage: 5, title: 'Список адресов', description: 'Client State', position: 'left-[550px] top-[444px] w-[354px] h-[160px]', border: 'border-[#41e786]' },
  { key: 'ui', stage: 5, title: 'UI-компонент', description: '', position: 'left-[1354px] top-[444px] w-[354px] h-[160px]', border: 'border-[#41e786]' },
  { key: 'add', stage: 6, title: 'Добавить адрес', description: '', position: 'left-[896px] top-[748px] w-[402px] h-[120px]', border: 'border-[#41e786]' },
] as const
</script>

<template>
  <div class="client-cache-diagram relative h-full font-body text-white" role="group" aria-label="Жизненный цикл серверного состояния: Backend, API, клиентский список адресов и UI">
    <div
      v-for="region in regions"
      :key="region.title"
      :data-region="region.title.toLowerCase()"
      class="absolute top-[288px] h-[616px] transition-opacity duration-500 ease-out motion-reduce:duration-0"
      :class="[region.position, revealClass(region.stage)]"
      :aria-hidden="stage < region.stage"
    >
      <p class="m-0 font-bold text-[40px] leading-[48px]">{{ region.title }}</p>
      <div class="absolute top-[68px] w-full h-[548px] box-border rounded-[32px] border-2 border-solid border-white/20" aria-hidden="true"></div>
    </div>

    <article
      v-for="node in nodes"
      :key="node.key"
      :data-node="node.key"
      class="absolute transition-opacity duration-500 ease-out motion-reduce:duration-0 box-border flex flex-col items-center justify-center gap-[16px] rounded-[24px] border-2 border-solid bg-white/5 px-[24px] text-center text-[32px] leading-[38.4px] backdrop-blur-[19px] [box-shadow:inset_-24px_-24px_64px_rgb(255_255_255_/_6%),inset_24px_24px_64px_rgb(0_0_0_/_40%)]"
      :class="[node.position, node.border, revealClass(node.stage)]"
      :aria-hidden="stage < node.stage"
    >
      <p class="m-0 w-full font-bold">{{ node.title }}</p>
      <p v-if="node.description" class="m-0 w-full font-normal text-muted">{{ node.description }}</p>
    </article>

    <!-- Native vector connectors remain editable code; blocks and labels are HTML. -->
    <svg class="absolute top-0 left-[-80px] pointer-events-none text-white opacity-[0.55]" width="1920" height="1080" viewBox="0 0 1920 1080" fill="none" aria-hidden="true">
      <g data-connection="addresses-to-api" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(4)">
        <path d="M250 604V680" stroke="currentColor" stroke-width="4" />
        <path d="M261.158 674.5L250 694.956L238.842 674.5H261.158Z" fill="currentColor" stroke="currentColor" />
      </g>
      <g data-connection="api-to-addresses" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(4)">
        <path d="M368 700V624" stroke="currentColor" stroke-width="4" />
        <path d="M379.158 629.5H356.842L368 609.043L379.158 629.5Z" fill="currentColor" stroke="currentColor" />
      </g>
      <g data-connection="http-get" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(5)">
        <path d="M486 728C562 728 584 524 614 524" stroke="currentColor" stroke-width="4" />
        <path d="M625.099 524L608.5 535.065V512.934L625.099 524Z" fill="currentColor" stroke="currentColor" />
      </g>
      <g data-connection="read" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(5)">
        <path d="M1420 524H1004" stroke="currentColor" stroke-width="4" />
        <path d="M1012 512L988 524L1012 536V512Z" fill="currentColor" />
      </g>
      <g data-connection="ui-to-add" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(6)">
        <path d="M1611 612C1611 808 1500 808 1398 808" stroke="currentColor" stroke-width="4" />
        <path d="M1403.5 819.158L1383.04 808L1403.5 796.841V819.158Z" fill="currentColor" stroke="currentColor" />
      </g>
      <g data-connection="invalidate" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(6)">
        <path d="M1177 738C1177 660 807 690 807 626" stroke="currentColor" stroke-width="4" />
        <path d="M818.191 631.5H795.809L807 609.118L818.191 631.5Z" fill="currentColor" stroke="currentColor" />
      </g>
      <g data-connection="http-post" class="transition-opacity duration-500 ease-out motion-reduce:duration-0" :class="revealClass(6)">
        <path d="M962 808C760 864 540 844 502 782" stroke="currentColor" stroke-width="4" stroke-dasharray="12 12" />
        <path d="M518.168 782.153L503.163 798.097L490.971 769.023L518.168 782.153Z" fill="currentColor" stroke="currentColor" />
      </g>
    </svg>

    <p data-label="HTTP GET" :class="revealClass(5)" :aria-hidden="stage < 5" class="transition-opacity duration-500 ease-out motion-reduce:duration-0 absolute top-[650px] left-[550px] w-[354px] m-0 text-[24px] leading-[28.8px] font-bold">HTTP GET</p>
    <p data-label="Read" :class="revealClass(5)" :aria-hidden="stage < 5" class="transition-opacity duration-500 ease-out motion-reduce:duration-0 absolute top-[474px] left-[1029px] w-[200px] m-0 text-center text-[24px] leading-[28.8px] font-bold">Read</p>
    <p data-label="Invalidate" :class="revealClass(6)" :aria-hidden="stage < 6" class="transition-opacity duration-500 ease-out motion-reduce:duration-0 absolute top-[632px] left-[896px] w-[354px] m-0 text-[24px] leading-[28.8px] font-bold">Invalidate</p>
    <p data-label="HTTP POST" :class="revealClass(6)" :aria-hidden="stage < 6" class="transition-opacity duration-500 ease-out motion-reduce:duration-0 absolute top-[868px] left-[550px] w-[280px] m-0 text-[24px] leading-[28.8px] font-bold">HTTP POST</p>
  </div>
</template>
