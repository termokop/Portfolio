<script setup>

</script>


<template>
  <div class="item">

    <div class="screen-shot">
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
}


.item:hover {
        background-color: #3d3d3d;
        border-end-end-radius: 20px;
        border-end-start-radius: 20px;
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
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

 @media (min-width: 1024px) {
  .item {
    padding: .5rem;
    width: 400px;
  }

}
</style>
