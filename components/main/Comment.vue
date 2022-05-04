<template>
  <el-card class='comment'>
    <div class='comment__header'>
      <span>Person name</span>
      <span>
        <i class='el-icon-time'></i>
        {{ new Date().toLocaleString() }}
      </span>
    </div>
    <div class='comment__text'>
      Lorem ipsum dolor sit amet.
    </div>
  </el-card>
</template>

<script>
export default {
  props: ['comment']
}
</script>

<style lang='scss' scoped>
  .comment {
    margin-bottom: 1rem;
  }

  .comment__header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.5rem;
    font-size: 0.8rem;
  }
</style>
