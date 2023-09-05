<script setup>
import vProjectItem from './vProjectItem.vue'

import {ref} from 'vue'
const projects = ref(
  [
    {
      id: 1,
      title: 'Tbilisea',
      screen_shot: 'https://www.wbcsd.org/var/site/storage/images/overview/news-insights/wbcsd-insights/accelerating-business-along-the-road-to-a-nature-positive-future/225091-1-eng-GB/Accelerating-business-along-the-road-to-a-nature-positive-future_i1140.jpg',
      details: 'Selling tickets for DJ-events',
      link_github: 'https://github.com/'
    }
  ]
)
</script>

<template>
  <vProjectItem v-for="project in projects" :key="project.id">
    <template #title>
      <h2>{{project.title}}</h2>  
    </template>
    <template #screen-shot>
      <img :src="project.screen_shot" :alt="project.title">
    </template>
    <template #links>
      <a :href="project.link_github" target="_blank">Github</a>  
    </template>

    Vue’s
    <a href="https://vuejs.org/" target="_blank" rel="noopener">official documentation</a>
    provides you with all information you need to get started.
  </vProjectItem>

</template>

<style scoped>

img {
  width: 100%;
}

</style>