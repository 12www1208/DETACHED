<script setup>
import video from '../../../assets/img/video_s.png'
const {item, index} = defineProps(['item', 'index']);
const text = item.text
const clicImg = () => {
  window.open(`https://vk.com/detachedproduction?w=wall-213692460_${item.id}`)
}
let img  = ''
if( item.attachments.length != 0 && item.attachments[0]['type'] == 'photo') {
  let mas  = item.attachments[0]['photo']['sizes']
  img = mas[mas.length -1]['url']
}
else if(item.attachments.length != 0 && item.attachments[0]['type'] == 'video') {
  img = video 
}

</script>

<template>
  <div class="newsBlock flex flex-col items-center space-y-4 w-full pt-4" >
    <h1 class="w-full text-white text-center mb-4 text-3xl">Новость {{ index + 1}}</h1>
    <p class="text-center text-white text-2xl">{{text}}</p>
    <img @click="clicImg" class="w-1/2 md:w-1/4 cursor-pointer" :src="img"/>
    <hr/>
  </div>
</template>
