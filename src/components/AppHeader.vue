<template>
 <nav class="navbar bg-light">
  <div class="container-fluid">
    <a class="navbar-brand d-flex" href="#">
      <img src="https://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="Logo" class="d-inline-block align-text-top">
      <h2>
        Yu-Gi-Oh Api
      </h2>
    </a>
  </div>
</nav>
</template>



<script>
import { createApp } from 'vue'
import AppHeader from './AppHeader.vue';
export default {
  name: "AppHeader"
  
}
</script>
 

<style lang="scss">

img{
  height: 30px;
  margin-right: 0.5rem;
}

</style>