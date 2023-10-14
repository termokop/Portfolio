<script setup>

  const zoom_picture = () => {
    alert('Zoom picture!')
  }

</script>


<template>
  <div class="item">

    <div class="screen-shot" @click="zoom_picture()">
      <slot name="screen-shot"></slot>
    </div>
    <div class="title">
      <slot name="title"></slot>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  width: 400px;
  height: 300px;
}

.title {
  width: fit-content;
  margin: auto;
}

.links {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.description {
  width: fit-content;
  margin: auto;
}

.screen-shot {
  width: 320px;
  margin: auto;
  height: 240px;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

 @media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }


  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
} 
</style>
