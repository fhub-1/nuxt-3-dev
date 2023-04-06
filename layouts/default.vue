<template>
  <div>
    <header class="shadow-md bg-white dark:bg-gray-900">
      <nav class="container mx-auto p-4 flex justify-between items-center">
        <NuxtLink to="/" class="font-bold">
          <img src="/logo.png" class="w-60 h-30" />
        </NuxtLink>
        <div class="flex md:hidden">
          <button
            @click="showMenu = !showMenu"
            class="text-gray-100 hover:text-gray-200 focus:outline-none focus:text-gray-100"
          >
            <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
              <path
                v-if="showMenu"
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M2.92 5.38l4.95-4.95a1 1 0 0 1 1.41 0l4.95 4.95a1 1 0 0 1-1.41 1.41L8.83 4.83l-4.24 4.24a1 1 0 1 1-1.41-1.41zm18.93 13.23l-4.95 4.95a1 1 0 0 1-1.41 0l-4.95-4.95a1 1 0 1 1 1.41-1.41l4.24 4.24 4.24-4.24a1 1 0 1 1 1.41 1.41z"
              />
              <path
                v-else
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M4 6h16v2H4V6zm0 5h16v2H4v-2zm16 4H4v2h16v-2z"
              />
            </svg>
          </button>
        </div>
        <div class="hidden md:flex">
          <ul class="flex gap-4">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/blog">Blog</NuxtLink></li>
            <!-- <li><NuxtLink to="/project">Project</NuxtLink></li> -->
          </ul>
        </div>
        <div class="md:hidden" :class="{ block: showMenu, hidden: !showMenu }">
          <ul class="mt-2">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/blog">Blog</NuxtLink></li>
            <!-- <li><NuxtLink to="/project">Project</NuxtLink></li> -->
          </ul>
        </div>
      </nav>
    </header>
    <!-- adding slog for the content of the page -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
};
</script>

<style scoped>
.router-link-exact-active {
  color: hsl(53, 96%, 49%);
}
</style>
