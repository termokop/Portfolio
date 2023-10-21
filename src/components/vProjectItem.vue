<script setup>

  const zoom_picture = () => {
    alert('Zoom picture!')
  }

</script>


<template>
  <div class="item">
    <div class="title">
      <slot name="title"></slot>
    </div>
    <div class="screen-shot" @click="zoom_picture()">
      <slot name="screen-shot"></slot>
    </div>
    <div class="details">
      <div class="links">
        <slot name="links"></slot>
      </div>
      <div class="description">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  width: 100%;
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
  width: 100%;
  margin: auto;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

 @media (min-width: 1024px) {
  .item {
    width: 400px;
    padding: 0.5rem;
  }
}
</style>
