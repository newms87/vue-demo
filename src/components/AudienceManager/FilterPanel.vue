<template>
  <div class="filterPanel">
    <Expander title="Settings"/>
    <Expander title="Location" subtitle="0 Applied"/>
    <Expander title="Filters" subtitle="4 Applied"/>
    <Expander title="Preferences" subtitle="10 Applied"/>
  </div>
</template>

<script>
import Expander from '../Expander.vue'

export default {
  name: 'FilterPanel',
  components: {
    Expander
  },
  props: {
  }
}
</script>

<style scoped>
  .filterPanel {
    border-right: 1px solid #cdd4e3;
    box-shadow: 2px 1px 3px 0 #cdd4e3;
    display: flex;
    flex: 0 0 25%;
    flex-direction: column;
    justify-content: flex-start;
  }
</style>
