<script setup>
import { ref } from 'vue';
import blockClipVue from './blockClip/blockClip.vue';
import preloader from '../ui/preloader/preloader.vue'
const show = ref(true)
const list = ref()
function test(result) {
  const data = result.videos
  list.value = data
  show.value = false
}

$.ajax({
  url: 'https://invidious.nerdvpn.de/api/v1/playlists/PLqF_eoGQvFAHuSMYiQdyxyz1Sb9v3-GPz',
  success: test
})

</script>

<template>
  <div class="clips pt-20  flex  flex-wrap space-x-10 justify-center">
    <preloader v-show="show"/>
    <blockClipVue v-for="item in list" :title="item.title" :video-id="item.videoId" :img="item.videoThumbnails[0].url" />
  </div>
</template>
