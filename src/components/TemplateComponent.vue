<template>
  <div class="templateComponent">
    <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'TemplateComponent',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .templateComponent {

  }
</style>
