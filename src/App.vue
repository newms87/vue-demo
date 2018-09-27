<template>
  <div class="app">
    <Banner title="company"/>
    <Toolbar />
    <AudienceManager/>
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  </div>
</template>

<script>
import Banner from './components/Banner.vue'
import Toolbar from './components/Toolbar.vue'
import AudienceManager from './components/AudienceManager/AudienceManager.vue'

export default {
  name: 'app',
  components: {
    AudienceManager,
    Banner,
    Toolbar
  }
}
</script>

<style>
.app {
  display: grid;
  grid-template-columns: 60px repeat(18, 1fr);
  grid-template-rows: 60px repeat(18, 1fr);
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
