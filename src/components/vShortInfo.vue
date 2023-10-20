<script setup>

import {ref} from 'vue'

const info = ref({
  name: 'Hruba Yurii',
  Location: 'Calgary, AB'
})


defineProps({
  role: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ role }}</h1>
    <div class="info">

      <span class="green">Name:</span> {{ info.name }}     
      <br> 
      <span class="green">Location:</span> {{ info.Location }}
      
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}


.info {
  letter-spacing: 2px;
  word-spacing: 4px;
  width: fit-content;
  margin: auto;
}


.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
  .info {
  letter-spacing: 2px;
  word-spacing: 4px;
  width: 100%;
}
}
</style>
