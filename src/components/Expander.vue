<template>
  <div class="expander">
    <div class="expander__left">
      <div class="expander__left--title">{{ title }}</div>
      <div class="expander__left--subtitle">{{ subtitle }}</div>
    </div>
    <div class="expander__right">
      <font-awesome-icon icon="angle-right" style="font-size: 16px;"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Expander',
  props: {
    title: String,
    subtitle: String
  }
}
</script>

<style scoped>
  .expander {
    align-items: center;
    border-bottom: 1px solid #CDD4E3;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    min-height: 36px;
    padding: 1rem;
  }

  .expander__left {
    display: flex;
    flex-direction: column;
  }

  .expander__left--title {
    color: #333;
  }

  .expander__left--subtitle {
    color: #788193;
    font-size: .75rem;
    font-style: italic;
    padding-top: .25rem;
  }

  .expander__right {

  }
</style>
