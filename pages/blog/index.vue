<template>
  <div class="px-6 py-4">
    <h2 class="text-xl font-semibold text-gray-100 mb-2">Blog post title</h2>
    <p class="text-gray-100 text-base">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sed dapibus leo nec
      ornare diam.</p>
  </div>
  <ul>
    <li v-for="{ _path: slug, title } in blogPosts" :key="slug">
      <NuxtLink :to="slug">{{ title }}</NuxtLink>
    </li>
  </ul>
</template>

<script setup lang="ts">
const blogPosts = await queryContent('/blog')
  .sort({ date: -1 }) // show latest articles first
  .where({ _partial: false }) // exclude the Partial files
  .find()
</script>
