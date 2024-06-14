<script setup>
import { reactive, ref } from 'vue';
import WidgetA from './components/componentWidgetA.vue'
import WidgetB from './components/componentWidgetB.vue'
import WidgetC from './components/componentWidgetC.vue'

const widgetCollection = {
  WidgetA, WidgetB, WidgetC
}

const dynamicComponent = widgetCollection['WidgetC'] // Using a string to dynamically select a component from a collection to display
const dynamicComponentData = reactive({ data: 'JSON loaded from DB' })
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  </header>

  <main>
    <component :is="dynamicComponent" :widgetData="dynamicComponentData" />
  </main>
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
