<template>
  <div class="banner">
    <div class="banner__title">{{ title }}</div>
    <UserMenu username="McNeill Media + Co"/>
  </div>
</template>

<script>
import UserMenu from './UserMenu.vue'

export default {
  name: 'Banner',
  props: {
    title: String
  },
  components: {
    UserMenu
  }
}
</script>

<style scoped>
  .banner {
    align-items: center;
    box-shadow: 0 3px 5px 0px #cdd4e3;
    display: flex;
    grid-column: 1/-1;
    grid-row: 1/2;
    justify-content: space-between;
    padding: 0 2rem;
    z-index: 1000;
  }
  .banner__title {
    color: #5faee1;
    font-size: 1.5rem;
    font-weight: bold;
  }
</style>
