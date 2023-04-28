<script setup>
const {videoId, title, img} = defineProps({
  'videoId': String,
  'title': String,
  'img': String
});
const clickClip = () => {
  console.log(videoId)
  window.open(`https://www.youtube.com/watch?v=${videoId}`)
}
</script>

<template>
  <div @click="clickClip" class="blockClip w-3/4  h-3/4 md:w-1/5 md:h-1/5 cursor-pointer text-white hover:text-hE">
    <img class="w-full h-full" :src="img" alt="">
    <h1 class=" w-full text-center mt-4 text-3xl font-Rubik">{{title}}</h1>
  </div>
</template>
