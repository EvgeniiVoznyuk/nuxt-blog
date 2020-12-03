<template>
  <el-card shadow="hover" :body-style="{ padding: 0 }" class="post">
    <header slot="header" class="post__header">
      <h3>Post title</h3>
      <small>
        <i class="el-icon-time" />
        {{ new Date().toLocaleString() }}
      </small>
    </header>
    <div class="post__body">
      <img
        src="https://tuhub.ru/sites/default/files/2018-02/vuejs-logo_0.jpg"
        alt="post-img"
        class="post__img"
      >
      <hr>
    </div>
    <footer class="post__footer">
      <el-button round @click="openPost">
        Открыть
      </el-button>
      <span class="post__comments">
        <i class="el-icon-message" />
        12
      </span>
    </footer>
  </el-card>
</template>

<script>
export default {
  methods: {
    openPost () {
      const id = 'test-id'
      this.$router.push(`/post/${id}`)
    }
  }
}
</script>

<style lang="scss" scoped>
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

  &__comments {
    cursor: pointer;
  }
}
</style>
