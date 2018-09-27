<template>
  <div class="toolbar">
    <div class="toolbar__item">
        <font-awesome-icon icon="globe-americas" style="font-size: 22px;"/>
    </div>
    <div class="toolbar__item">
        <font-awesome-icon icon="bullhorn" style="font-size: 18px;"/>
    </div>
    <div class="toolbar__item">
        <font-awesome-icon icon="file-pdf" style="font-size: 20px;"/>
    </div>
    <div class="toolbar__item">
        <font-awesome-icon icon="file-image" style="font-size: 20px;"/>
    </div>
    <div class="toolbar__item">
        <font-awesome-icon icon="dollar-sign" style="font-size: 24px;"/>
    </div>
    <div class="toolbar__item">
        <font-awesome-icon icon="question-circle" style="font-size: 22px;"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Toolbar',
  props: {
    title: String
  }
}
</script>

<style scoped>
  .toolbar {
    align-items: center;
    background: #eef0f5;
    color: #5faee1;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    grid-row: 2/-1;
    grid-column: 1/2;
    padding-top: 1rem;
    z-index: 500;
  }

  .toolbar__item {
    align-items: center;
    color: #788193;
    display: flex;
    height: 25px;
    justify-content: center;
    margin: .75rem;
    transition: color .75s ease;
  }

  .toolbar__item:hover {
    color: #333;
  }
</style>
