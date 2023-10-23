<script setup>
import { RouterLink, RouterView } from 'vue-router'
import vShortInfo from './components/vShortInfo.vue'
import vLinks from './components/vLinks.vue';
</script>

<template>
  <header>
    <img alt="Picture" class="logo" src="@/assets/myPhoto.jpg" width="150" height="150" />

    <div class="wrapper">
      <v-short-info role="Web Developer" />

      <nav>
        <RouterLink to="/">Projects</RouterLink>
        <RouterLink to="/education">Education</RouterLink>
        <RouterLink to="/about">About me</RouterLink>
      </nav>
    </div>
  </header>
  <div class="content">
    <RouterView />
  </div>



  <footer>
    <v-links></v-links>
  </footer>


</template>

<style scoped>
header {
  line-height: 1.5;
  width: fit-content;
  margin: auto;
  padding: 0;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  border-radius: 50%;
}

nav {
  width: 100%;
  font-size: 16px;
  text-align: center;
  margin: auto;
  padding-top: 1rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

footer {
  position: static;
  display: flex;
  justify-content: center;
  align-content: flex-start;
  bottom: 0;
  max-width: 1360px;
  width: 100%;
  padding: 0;
  height: 180px;
}

.content {
  margin-bottom: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
   /* padding-right: calc(var(--section-gap) / 2);*/
  }

  footer {
  position: fixed;
  display: flex;
  justify-content: center;
  align-content: flex-start;
  bottom: -10px;
  max-width: 1360px;
  width: 100%;
  padding: 0;
  height: 180px;
  margin-bottom: 10px;
  background-color: #1d1d1d;
}

  .content {
    margin-bottom: 180px;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;
  }
}
</style>
