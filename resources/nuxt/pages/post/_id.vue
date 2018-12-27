<template>
  <div>
    <p>記事の本文{{ $route.params.id }}</p>
    <article v-if="post">
        <h1 class="title">{{ post.title }}</h1>
        <p> ここに記事の本文が入ります。 </p>
    </article>
  </div>
</template>

<script >
export default {
    data() {
        return {
            post: null
        }
    },
    mounted() {
        for (let post of this.$store.state.posts) {
            if (post.id == this.$route.params.id) {
                this.post = post;
            }
        }
        if (!this.post) {
            this.$router.push("/");
        }
    }
}
</script>