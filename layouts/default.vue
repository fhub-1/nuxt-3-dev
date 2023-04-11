<template>
  <div>

    <head>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
    </head>
    <header class="shadow-md dark:bg-gray-900">

      <nav class="container mx-auto p-4 flex justify-between items-center">
        <NuxtLink to="/" class="font-bold flex items-center">
          <img v-bind:src="logo" class="mr-2" width="240" height="240" />
        </NuxtLink>
        <div class="flex items-center md:hidden">
          <button @click="showMenu = !showMenu"
            class="text-gray-100 hover:text-gray-200 focus:outline-none focus:text-gray-100">
            <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
              <path v-if="!showMenu" fill-rule="evenodd" clip-rule="evenodd"
                d="M4 6h16v2H4V6zm0 5h16v2H4v-2zm16 4H4v2h16v-2z" />
              <path v-else fill-rule="evenodd" clip-rule="evenodd"
                d="M3.293 4.293a1 1 0 0 1 1.414 0L12 10.586l7.293-7.293a1 1 0 1 1 1.414 1.414L13.414 12l7.293 7.293a1 1 0 1 1-1.414 1.414L12 13.414l-7.293 7.293a1 1 0 0 1-1.414-1.414L10.586 12 3.293 4.707a1 1 0 0 1 0-1.414z" />
            </svg>
          </button>


        </div>
        <div class="hidden md:flex">
          <ul class="flex gap-4">
            <li class="fas fa-home">
              <NuxtLink to="/" :class="{ 'router-link-exact-active': $route.path === '/' }">Home</NuxtLink>
            </li>
            <li class="fas fa-info-circle">
              <NuxtLink to="/about" :class="{ 'router-link-exact-active': $route.path === '/about' }">About</NuxtLink>
            </li>
            <li class="fas fa-blog">
              <NuxtLink to="/blog" :class="{ 'router-link-exact-active': $route.path === '/blog' }">Blog</NuxtLink>
            </li>
          </ul>
        </div>
        <div class="md:hidden" :class="{ 'block': showMenu, 'hidden': !showMenu }">
          <ul class="mt-2">
            <li>
              <NuxtLink to="/" :class="{ 'router-link-exact-active': $route.path === '/' }">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" :class="{ 'router-link-exact-active': $route.path === '/about' }">About</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/blog" :class="{ 'router-link-exact-active': $route.path === '/blog' }">Blog</NuxtLink>
            </li>
          </ul>
        </div>
      </nav>
    </header>
    <div class="container mx-auto p-4">
      <slot />
    </div>
    <Footer />
    <button @click="toggleDarkMode" class="bg-gray-300 dark:bg-gray-600 rounded-full p-2">
      <span class="text-gray-800 dark:text-gray-300">
        {{ darkMode ? 'Light' : 'Dark' }}
      </span>
    </button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      showMenu: false,
      logo: "/logo-light.svg",
      logoWidth: 60,
      logoHeight: 30,
      darkMode: false
    };
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      document.documentElement.classList.toggle('dark');
    },
  },
  computed: {
    logoSrc() {
      return this.$vuetify.theme.dark ? '/logo-dark.png' : '/logo-light.svg'
    },
  },
};
</script>

<style scoped>
.router-link-exact-active {
  color: hsl(53, 96%, 49%);
}

.dark-mode {
  --bg-color: #1f2937;
  --text-color: #f3f4f6;
}

body.dark-mode {
  background-color: var(--bg-color);
  color: var(--text-color);
}
</style>
