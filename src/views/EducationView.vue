<script setup>

  import vEducationInfo from '../components/vEducationInfo.vue';

</script>

<template>
  <div class="about">
    <vEducationInfo></vEducationInfo>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
