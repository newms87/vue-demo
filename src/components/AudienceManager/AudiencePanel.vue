<template>
  <div class="audiencePanel">
    <div>{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'AudiencePanel',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .audiencePanel {
    border: 1px solid #CDD4E3;
    border-radius: 3px;
    height: 100%;
  }
</style>
