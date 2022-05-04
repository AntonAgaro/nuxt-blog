<template>
  <div class='error-layout'>
    <div class='error-content'>
      <h1 class='error-title'>Ошибка 404</h1>
      <nuxt-link to='/'>Вернуться на главную</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
  .error-layout {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .error-title {
    color: rgb(145, 6, 6);
    margin-bottom: 1rem;
  }

  .error-content {
    padding-top: 4rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
