<template>
  <div class="shadow-md border border-gray-500 rounded-md py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:mx-0">
        <h2 class="text-3xl font-bold tracking-tight text-gray-100 sm:text-4xl">From the blog</h2>
        <p class="mt-2 text-lg leading-8 text-gray-100">Learn how to grow your business with our expert advice.</p>
      </div>
      <div
        class="mx-auto mt-10 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 border-t border-gray-200 pt-10 sm:mt-16 sm:pt-16 lg:mx-0 lg:max-w-none lg:grid-cols-3">
        <article class="flex max-w-xl flex-col items-start justify-between">

          <li v-for="{ _path: slug, title, autho, date } in blogPosts" :key="slug">
            <NuxtLink :to="slug">{{ title }}</NuxtLink>
            <!-- <p class="text-sm text-gray-400 ml-auto">{{ new Date(date).toLocaleDateString() }}</p> -->
          </li>
        </article>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const blogPosts = await queryContent('/blog')
  .sort({ date: -1 }) // show latest articles first
  .where({ _partial: false }) // exclude the Partial files
  .find()
</script>
