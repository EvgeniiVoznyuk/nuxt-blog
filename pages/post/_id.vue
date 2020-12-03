<template>
  <article class="post">
    <header class="post__header">
      <div class="post__title">
        <h1>Post title</h1>
        <nuxt-link to="/" />
        <i class="el-icon-back" />
      </div>
      <div class="post__info">
        <small>
          <i class="el-icon-time" />
          {{ new Date().toLocaleString() }}
        </small>
        <small>
          42
          <i class="el-icon-view" />
        </small>
      </div>
      <div class="post__img">
        <img
          src="https://tuhub.ru/sites/default/files/2018-02/vuejs-logo_0.jpg"
          alt="post-img"
          class="post__img"
        >
      </div>
    </header>
    <main class="post__main">
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, accusantium?</p>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, accusantium?</p>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, accusantium?</p>
    </main>
  </article>
</template>

<script>
export default {
  validate ({ params }) {
    return !!params.id
  }
}
</script>

<style lang="scss" scoped>
.post {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;

  &__title {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1rem;
    align-items: center;
  }

  &__info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.5rem;
  }
}
</style>
