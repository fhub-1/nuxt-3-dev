<template>
  <section class="pt-10 overflow-hidden md:pt-0 sm:pt-16 2xl:pt-16">
    <div class="px-4 mx-auto sm:px-6 lg:px-8 max-w-7xl">
      <div class="grid items-center grid-cols-1 md:grid-cols-2">
        <div>
          <h2 class="text-3xl font-bold leading-tight sm:text-4xl lg:text-5xl">
            Hey 👋 I am <br class="block sm:hidden" />Joseph Kitheka
          </h2>
          <p
            class="max-w-lg mt-3 text-xl leading-relaxed dark:text-gray-100 md:mt-8"
          >
            Full Stack Developer and YouTube Content Creator. Passionate about
            tech and video creation. Always looking to learn new things!
          </p>

          <p class="mt-4 text-xl dark:text-gray-100 md:mt-8">
            <span class="relative inline-block">
              <span
                class="absolute inline-block w-full bottom-0.5 h-1 bg-yellow-300"
              ></span>
              <span class="relative"> Have a question? </span>
            </span>
            <br class="block sm:hidden" />Ask me on
            <NuxtLink
              to="https://twitter.com/josehub121"
              title=""
              class="transition-all duration-200 text-sky-500 hover:text-sky-600 hover:underline"
              >Twitter
            </NuxtLink>
          </p>
        </div>

        <div class="relative">
          <img
            class="relative xl:max-w-lg xl:mx-auto 2xl:origin-bottom 2xl:scale-110 rounded-md sm:mt-10"
            src="/banner.png"
            alt="banner"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="stylus" scoped></style>
