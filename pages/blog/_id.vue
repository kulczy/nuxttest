<template>
  <section>
    <nuxt-link to="/blog">back</nuxt-link>
    <h1>Blog: {{ post.title }}</h1>
    <p>{{ post.body }}</p>
  </section>
</template>

<script>
export default {
  async asyncData ({ params }) {
    const query = await fetch(`https://jsonplaceholder.typicode.com/posts/${params.id}`);
    const post = await query.json();
    return { post };
  }
}
</script>

<style>
</style>
