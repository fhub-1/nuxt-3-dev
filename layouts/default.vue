<template>
    <div>
   <header class="shadow-sm bg-white ">
       <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink to="/" class="font-bold">Learn with joseph</NuxtLink>
        <ul class="flex gap-4">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/blog">Blog</NuxtLink></li>
            <!-- <li><NuxtLink></NuxtLink></li> -->
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
.router-link-exact-active{
      color: hsla(37, 98%, 49%, 0.999);
 }
</style>