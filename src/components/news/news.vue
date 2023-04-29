<script setup>
import { onBeforeMount, ref } from 'vue';
import newsBlock from './newsBlock/newsBlock.vue'
import preloaderVue from '../ui/preloader/preloader.vue';
const token = '2f5488e22f5488e22f5488e2982c47489622f542f5488e24b1366eff1966329a5476123'
const verison = '5.131'
const show = ref(false)
const list = ref('')
function test(result) {
  const data = result.response.items
  console.log(data)
  list.value = data
  show.value = true
}

onBeforeMount(() => {
  $.ajax({
    url: 'https://api.vk.com/method/wall.get',
    data: {
      owner_id: '-213692460',
      domain: 'detachedproduction',
      count: 50,
      filter: 'all',
      access_token: token,
      v: verison
    },
    dataType: 'jsonp',
    success: test
  })
})


</script>

<template>
  <div class="news overflow-x-hidden">
    <preloaderVue v-show="!show"/>
    <newsBlock v-for="(items, index) in list" :item="items" :index="index"  />
  </div>
</template>


