<template>
  <div class="resultsPanel">
    <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'ResultsPanel',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .resultsPanel {

  }
</style>
