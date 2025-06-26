<script setup>
import Calculateur from './components/Calculateur.vue';
import CalcMemory from './components/CalcMemory.vue';
import IconSupport from './components/icons/IconSupport.vue';
import { ref } from 'vue';

const memory = ref([]);
</script>

<template>
  <IconSupport />
  <Calculateur @calculate="c => memory.push(c)"/>
  <CalcMemory :memory />
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
