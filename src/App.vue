<script setup>
import { ref, shallowRef } from 'vue';
import Header from './components/header/header.vue';
import Navbar from './components/navbar/navbar.vue';
import News from './components/news/news.vue';

const components = shallowRef([
  Header,
  News
])
const componentId = ref(0)
</script>

<template>
  <div class="main-conteiner bg-d22">
    <Navbar @click-menu-item="(item) => componentId = item"/>
    <component :is="components[componentId]"></component>
  </div>
</template>
