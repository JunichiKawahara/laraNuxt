
<template>
  <div>
    <h1 class="title">My Blog App</h1>
    <p>
      NUXT.JS 入門 #1 – NUXT.JS によるブログアプリ制作
      <a target="_blank" href="https://www.chatbox.blog/2018/03/26/nuxt-js-start-1/">https://www.chatbox.blog/2018/03/26/nuxt-js-start-1/</a>
    </p>

    <ul>
        <li v-for="post in posts" :key="post.id">
          <router-link :to="`/post/${post.id}`">{{post.title}}</router-link>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
    }
  },
  computed: {
    posts() {
      return this.$store.state.posts;
    }
  },
  mounted() {
    this.$store.dispatch("load");
  }
}
</script>