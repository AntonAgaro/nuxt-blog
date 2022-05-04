<template>
  <el-card
    shadow='hover'
    :body-style='{padding: 0}'
    class='post'
  >
    <header class='post__header' slot='header'>
      <h3>Post Title</h3>
      <small>
        <i class='el-icon-time'></i>
        {{ new Date().toLocaleString() }}
      </small>
    </header>
    <div class='post__body'>
      <img class='post__img'
           src='https://www.alpadia.com/sites/default/files/styles/hero_banner_md/public/school/featured/berlin-school-hero-1.jpg?itok=tAS8nW9K'
           alt='post image'
      >
    </div>
    <footer class='post__footer'>
      <el-button round @click='openPost'>Открыть</el-button>
      <span>
        <i class='el-icon-message'></i>
        12
      </span>
    </footer>
  </el-card>
</template>

<script>
export default {
  methods: {
    openPost() {
      const id = 'test-id';
      this.$router.push(`/post/${id}`);
    }
  }
}
</script>

<style lang='scss' scoped>
  .post {
    margin-bottom: 1.5rem;

    &__header {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &__img {
      width: 100%;
      height: auto;
    }

    &__footer {
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
</style>
