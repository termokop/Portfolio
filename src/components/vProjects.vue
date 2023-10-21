<script setup>
import vProjectItem from './vProjectItem.vue'

import {ref} from 'vue'
const projects = ref(
  [
    {
      id: 1,
      title: 'Tbilisea',
      screen_shot: 'https://www.wbcsd.org/var/site/storage/images/overview/news-insights/wbcsd-insights/accelerating-business-along-the-road-to-a-nature-positive-future/225091-1-eng-GB/Accelerating-business-along-the-road-to-a-nature-positive-future_i1140.jpg',
      technologies: 'Quasar, Vue3, RestAPI, PHP, SQL',
      link_github: 'https://github.com/',
      link_project: 'https://ukrge.site/tbilisea/'
    },
    {
      id: 2,
      title: 'House Keeping',
      screen_shot: 'https://www.wbcsd.org/var/site/storage/images/overview/news-insights/wbcsd-insights/accelerating-business-along-the-road-to-a-nature-positive-future/225091-1-eng-GB/Accelerating-business-along-the-road-to-a-nature-positive-future_i1140.jpg',
      technologies: 'Vue3, RestAPI, PHP, SQL',
      link_github: 'https://github.com/termokop/HouseKeeping',
      link_project: 'https://ukrge.site/housekeeping/'
    },
    {
      id: 3,
      title: 'Cryptonomicon',
      screen_shot: 'https://www.wbcsd.org/var/site/storage/images/overview/news-insights/wbcsd-insights/accelerating-business-along-the-road-to-a-nature-positive-future/225091-1-eng-GB/Accelerating-business-along-the-road-to-a-nature-positive-future_i1140.jpg',
      technologies: 'Vue3, Tailwind',
      link_github: 'https://github.com/termokop/cryptonomicon',
      link_project: 'termokop.github.io/cryptonomicon/'
    }
  ]
)
</script>

<template>
  <div class="projects-view">
    <vProjectItem v-for="project in projects" :key="project.id">
      <template #title>
        <h2>{{project.title}}</h2>  
      </template>
      <template #screen-shot>
        <img :src="project.screen_shot" :alt="project.title">
      </template>
      <template #links>
        <a :href="project.link_github" target="_blank">Github</a>  
        <a :href="project.link_project" target="_blank">Project</a>
        <a href="#">Details</a>
      </template>
        <p>
          {{ project.technologies }}
        </p>
    </vProjectItem>
  </div>

</template>

<style scoped>

img {
  width: 100%;
}

.projects-view {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>