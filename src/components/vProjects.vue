<script setup>
import vProjectItem from './vProjectItem.vue'

import {ref} from 'vue'
const projects = ref(
  [
    {
      id: 1,
      title: 'UkrGe',
      screen_shot: 'src/assets/screens/ukrge.png',
      technologies: 'Quasar, Vue3, RESTful API, PHP, SQL',
      link_github: 'https://github.com/termokop/Tbilisea/',
      link_project: 'https://www.ukrge.site/tbilisea/'
    },
    {
      id: 1,
      title: 'Tbilisea',
      screen_shot: 'src/assets/screens/tbilisea.png',
      technologies: 'Quasar, Vue3, RESTful API, PHP, SQL',
      link_github: 'https://github.com/termokop/Tbilisea/',
      link_project: 'https://www.ukrge.site/tbilisea/'
    },
    {
      id: 2,
      title: 'House Keeping',
      screen_shot: 'src/assets/screens/housekeeping.png',
      technologies: 'Vue3, RESTful API, PHP, SQL',
      link_github: 'https://github.com/termokop/HouseKeeping',
      link_project: 'https://ukrge.site/housekeeping/'
    },
    {
      id: 3,
      title: 'Cryptonomicon',
      screen_shot: 'src/assets/screens/cryptomomicon.png',
      technologies: 'Vue3, Tailwind, SharedWorker, WebSocket',
      link_github: 'https://github.com/termokop/cryptonomicon',
      link_project: 'https://termokop.github.io/cryptonomicon/'
    },
    {
      id: 4,
      title: 'VIY',
      screen_shot: "src/assets/screens/viy.png",
      technologies: 'Quasar, Vue3, RESTful API, SQL',
      link_github: 'https://github.com/termokop/viy',
      link_project: 'https://ukrge.site/viy/'
    },
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
        <div class="screenshot">
          <img :src="project.screen_shot" :alt="project.title"/>
        </div>
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

.screenshot {
  height: 250px;
  border: white 3px solid;
  overflow-y: hidden;
  border-radius: 5px;
  display: flex;
}

img {
  width: 100%;
}

.projects-view {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>