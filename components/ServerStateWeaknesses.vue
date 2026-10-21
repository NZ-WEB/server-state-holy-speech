<script setup lang="ts">
const problems = [
  {
    number: '01',
    title: 'Ключи требуют дисциплины',
    description: ['Нужно договориться, как называть и собирать query key ', 'для каждого среза данных'],
    node: '90:4167',
  },
  {
    number: '02',
    title: 'Контроль инвалидаций',
    description: ['После каждой мутации нужно точно определить, какие данные больше нельзя считать свежими'],
    node: '90:4169',
  },
  {
    number: '03',
    title: 'Широкое API',
    description: ['Query Cache доступен отовсюду – его легко размазать по компонентам, Store и роутеру'],
    node: '90:4171',
  },
] as const
</script>

<template>
  <section class="server-state-weaknesses" data-node="90:4166" aria-label="Слабые стороны Server State">
    <template v-for="(problem, index) in problems" :key="problem.number">
      <article class="weakness-row" :data-node="problem.node">
        <p class="weakness-number font-heading">{{ problem.number }}</p>
        <div class="weakness-copy font-body">
          <h2 class="weakness-title">{{ problem.title }}</h2>
          <div class="weakness-description">
            <p v-for="line in problem.description" :key="line" class="weakness-description-line">{{ line }}</p>
          </div>
        </div>
      </article>
      <div v-if="index < problems.length - 1" class="weakness-separator" aria-hidden="true" />
    </template>
  </section>
</template>

<style scoped>
.server-state-weaknesses {
  display: flex;
  width: 1760px;
  flex-direction: column;
  align-items: flex-end;
  gap: 40px;
  overflow: clip;
}

.weakness-row {
  display: flex;
  width: 100%;
  flex-shrink: 0;
  align-items: center;
  gap: 64px;
  overflow: clip;
  word-break: break-word;
}

.weakness-number {
  width: 116px;
  height: 95px;
  flex-shrink: 0;
  margin: 0;
  color: #ed0f00;
  font-size: 80px;
  font-weight: 900;
  line-height: 0.9;
  letter-spacing: -1.6px;
}

.weakness-copy {
  display: flex;
  width: 1010px;
  flex-shrink: 0;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  gap: 8px;
  font-variation-settings: 'YTLC' 500, 'wdth' 100;
}

.weakness-title {
  width: 100%;
  margin: 0;
  color: #fff;
  font-size: 32px;
  font-weight: 700;
  line-height: 1.1;
}

.weakness-description {
  width: 100%;
  color: rgb(255 255 255 / 69%);
  font-size: 30px;
  font-weight: 400;
  line-height: 38px;
  white-space: pre-wrap;
}

.weakness-description-line {
  margin: 0;
  line-height: 38px;
}

.weakness-separator {
  width: 1757px;
  height: 2px;
  flex-shrink: 0;
  background: linear-gradient(to right, rgb(255 255 255 / 20%), rgb(255 255 255 / 0%));
}
</style>
