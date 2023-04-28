<script setup>
const emits = defineEmits([ 'click-menu-item' ]);
</script>

<template>
  <nav class="h-16 bg-black flex   w-full items-center fixed z-50 justify-center" >
    <ul>
      <li @click="emits('click-menu-item', 0)" class="menu-item"><a href="#">Главная</a></li>
      <li @click="emits('click-menu-item', 1)" class="menu-item"><a href="#">Наш состав</a></li>
      <li @click="emits('click-menu-item', 2)" class="menu-item"><a href="#">Новости</a></li>
      <li @click="emits('click-menu-item', 3)" class="menu-item"><a href="#">Клипы</a></li>
    </ul>
  </nav>
</template>
