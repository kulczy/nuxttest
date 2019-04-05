<template>
  <section>
    <h1>Blog</h1>
    <div class="card card-body mb-3" v-for="post in posts" :key="post.id">
      <h4><nuxt-link :to="{ path: `/blog/${post.id}` }">{{ post.title }}</nuxt-link></h4>
      <p>{{ post.body }}</p>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData ({ params }) {
    const query = await fetch('https://jsonplaceholder.typicode.com/posts');
    const posts = await query.json();
    return { posts };
  }
}
</script>

<style>
</style>
