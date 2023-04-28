<script setup>
import Tihon from './../../assets/img/piople/Tihon.jpg'
import Ded from '../../assets/img/piople/Ded.jpg'
import Ela from '../../assets/img/piople/Ela.jpg'
import Alexad from '../../assets/img/piople/Alexandar.jpg'
import Danil from '../../assets/img/piople/Daniil.jpg'
</script>

<template>
  <div class="sostav flex md:h-screen flex-col items-center justify-between md:flex-row" >
    <div class="piople">
      <a href="https://vk.com/mannequinofdepressionn">
        <img  :src="Ded" alt="">
      </a>
      <h1 >Dead Mephistopheles - вокал</h1>
    </div>
    <div class="piople ">
      <a href="https://vk.com/worlddrumhunter">
        <img   :src="Ela" alt="">
      </a>
      <h1>Элайджа - барабаны</h1>
    </div>
    <div class="piople">
      <a href="https://vk.com/brain__death">
        <img  :src="Tihon" alt="">
      </a>
      <h1>Тихон - басс/электрогитара, бэк вокал</h1>
    </div>
    <div class="piople ">
      <a href="https://vk.com/udin.rook">
        <img  :src="Alexad" alt="">
      </a>
      <h1 >Александр Юдин - электрогитара, электроакустика , бэк вокал</h1>
    </div>
    <div class="piople ">
      <a href="https://vk.com/danilsvetkov">
        <img  :src="Danil" alt="">
      </a>
      <h1>Данил Цветков - гитара</h1>
    </div>
  </div>
</template>

<style scoped>
  img {
    image-rendering: optimizeQuality;
    width: 300px;
    height: 300px;
  }
  h1 {
    @apply w-3/4;
  }
</style>
