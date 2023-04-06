<template>
  <div>
    <h1>My Blog</h1>
    <ul>
      <li v-for="post in posts" :key="post.slug">
        <nuxt-link :to="`/blog/${post.slug}`">{{ post.title }}</nuxt-link>
        <p>{{ post.description }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData() {
    const posts = await this.$content("blog").sortBy("date", "desc").fetch();
    return {
      posts,
    };
  },
};
</script>
