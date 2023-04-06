<template>
  <div>
    <header class="shadow-md bg-white dark:bg-gray-900">
      <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink to="/" class="font-bold">
          <img src="/logo.png" class="w-60 h-30" />
        </NuxtLink>
        <ul class="flex gap-4">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/Blog">Blog</NuxtLink></li>
          <!-- <li><NuxtLink to="/project">Project</NuxtLink></li> -->
        </ul>
      </nav>
    </header>
    <!-- adding slog for the content of the page -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <Footer />
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: hsl(53, 96%, 49%);
}
</style>
