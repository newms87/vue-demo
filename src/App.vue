<template>
	<div class="app">
		<Banner title="company"/>
		<Toolbar/>
		<AudienceManager/>
		<!-- <img alt="Vue logo" src="./assets/logo.png"> -->
	</div>
</template>

<script>
  import Banner from './components/Banner.vue';
  import Toolbar from './components/Toolbar.vue';
  import AudienceManager from './components/AudienceManager/AudienceManager.vue';

  export default {
    name:       'app',
    components: {
      AudienceManager,
      Banner,
      Toolbar
    }
  };
</script>

<style>
	.app {
		display: grid;
		grid-template-columns: 60px auto;
		grid-template-rows: 60px auto;
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		height: 100%;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		width: 100%;
	}
</style>
