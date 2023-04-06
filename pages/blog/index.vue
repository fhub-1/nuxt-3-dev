<template>
  <div>
    <h1 class="text-4xl font-bold mb-5 border-b-[5px] w-[180px] border-indigo-600 pb-2">Blog</h1>
    <div class="grid grid-cols-1 gap-10">
      <div v-for="post in posts" :key="post.slug">
        <h2 class="text-2xl font-bold mb-2">{{ post.title }}</h2>
        <p class="text-gray-500 mb-4">{{ post.description }}</p>
        <div v-html="$nuxtContent(post.slug).toc"></div>
        <div v-html="$nuxtContent(post.slug).text"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const posts = await $content('blog').sortBy('date', 'desc').fetch()
    return { posts }
  }
}
</script>
