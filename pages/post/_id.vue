<template>
  <article class='post'>
    <header class='post__header'>
      <div class='post__title'>
        <h1>Post title</h1>
        <nuxt-link to='/'>
          <i class='el-icon-back'></i>
        </nuxt-link>
      </div>
      <div class='post__info'>
        <small>
          <i class='el-icon-time'></i>
          {{ new Date().toLocaleString() }}
        </small>
        <small>
          <i class='el-icon-view'></i>
          42
        </small>
      </div>
      <div class='post__image'>
        <img class='post__img' src='https://www.alpadia.com/sites/default/files/styles/hero_banner_md/public/school/featured/berlin-school-hero-1.jpg?itok=tAS8nW9K' alt='post-img'>
      </div>
    </header>
    <main class='post__content'>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae inventore quasi voluptatum. Dolore dolores facilis minima quibusdam sapiente. Assumenda explicabo nisi nulla. Amet animi dicta eos eveniet nostrum obcaecati rem.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae inventore quasi voluptatum. Dolore dolores facilis minima quibusdam sapiente. Assumenda explicabo nisi nulla. Amet animi dicta eos eveniet nostrum obcaecati rem.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Beatae inventore quasi voluptatum. Dolore dolores facilis minima quibusdam sapiente. Assumenda explicabo nisi nulla. Amet animi dicta eos eveniet nostrum obcaecati rem.</p>
    </main>
    <footer>
      <app-comment-form/>
       <div class='comments' v-if='true'>
          <app-comment
            v-for='comment in 4'
            :key='comment'
            :comment='comment'
          />
       </div>
        <div class='text-center' v-else>
          Комментариев нет
        </div>
    </footer>
  </article>
</template>

<script>
import AppCommentForm from '~/components/main/CommentForm';
import AppComment from '~/components/main/Comment';
  export default {
    validate({params}) {
      return !!params.id
    },
    components: {
      AppComment,
      AppCommentForm
    }
  }
</script>

<style lang='scss' scoped>
  .post {
    max-width: 600px;
    margin: 0 auto;

    &__title, &__info {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1rem;
    }

    &__info {
      margin-bottom: 0.5rem;
    }

    &__img {
      width: 100%;
      height: auto;
    }

    &__header {
      margin-bottom: 1.5rem;
    }

    &__content {
      margin-bottom: 2rem;
    }
  }
</style>
