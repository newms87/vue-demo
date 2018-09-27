<template>
  <div class="userMenu">
    <div class="userMenu__name">{{ username }}</div>
    <div class="userMenu__avatar">
      <font-awesome-icon icon="user-circle" style="font-size: 24px;"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserMenu',
  props: {
    username: String
  }
}
</script>

<style scoped>
  .userMenu {
    align-items: center;
    border: 1px solid #cdd4e3;
    border-radius: 4px;
    color: #788193;
    cursor: pointer;
    display: flex;
    padding: .5rem .75rem;
    transition: background .75s ease;
  }

  .userMenu:hover {
    background: #C9CCD3;
  }

  .userMenu__name {
    padding-right: .75rem;
  }

  .userMenu__avatar {
    align-items: center;
    display: flex;
    justify-content: center;
  }
</style>
