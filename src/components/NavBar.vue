<template>
  <div class="menu">
    <h1 class="header">Best Places</h1>
    <div>
      <a class="link">To Eat</a>
      <a class="link">To Explore</a>
      <a class="link">To Shop</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style scoped lang="scss">
  .menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 0;
    width: 100%;
    background-color: rgb(225, 236, 255);
  }
  .header {
    font-family: Calling Heart;
    font-weight: normal;
    font-size: 40px;
    color: black;
    margin-left: 16px;
  }
  .link {
    cursor: pointer;
    font-size: 14px;
    padding: 8px 16px;
    &:not(:last-child) {
      border-right: 1px solid rgb(145, 145, 145);
    }
  }
</style>
