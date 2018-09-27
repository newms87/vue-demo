<template>
  <div class="pageHeader">
    <div class="pageHeader__title">{{ title }}</div>
    <Button label="Save Audience"/>
  </div>
</template>

<script>
import Button from './Button.vue'

export default {
  name: 'PageHeader',
  props: {
    title: String
  },
  components: {
    Button
  }
}
</script>

<style scoped>
  .pageHeader {
    align-items: center;
    border-bottom: 2px solid #cdd4e3;
    display: flex;
    height: 65px;
    justify-content: space-between;
    padding-bottom: 1rem;
  }

  .pageHeader__title {
    color: #333;
    font-size: 1.5rem;
    font-weight: bold;
  }
</style>
