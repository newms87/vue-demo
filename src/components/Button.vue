<template>
  <div class="button">
    <div>{{ label }}</div>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    label: String
  }
}
</script>

<style scoped>
  .button {
    border: 2px solid #53bb77;
    color: #53bb77;
    cursor: pointer;
    border-radius: 4px;
    padding: .75rem;
    transition: background .5s ease;
  }

  .button:hover {
    background: #CBEAD6;
  }
</style>
