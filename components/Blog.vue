<template>
  <section class="bg-white px-5 py-32" id="blog">
    <div class="container mx-auto">
      <h2
        class="text-4xl font-bold mb-10 border-b-[5px] w-[180px] border-indigo-600 pb-2"
      >
        Blog
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
        <div
          v-for="(post, index) in posts"
          :key="index"
          class="bg-gray-100 p-5 rounded-md"
        >
          <img :src="post.image" :alt="post.title" class="mb-5 rounded-md" />
          <h3 class="text-2xl font-bold mb-2">{{ post.title }}</h3>
          <p class="text-gray-600 mb-5">{{ post.description }}</p>
          <div class="text-right">
            <a
              :href="post.link"
              target="_blank"
              rel="noopener noreferrer"
              class="px-5 py-2 bg-indigo-600 text-white font-bold hover:bg-indigo-700"
            >
              Read more
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {
          title: "Lorem ipsum dolor sit amet",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce ut aliquam quam, eu ullamcorper augue. Sed quis massa in eros tristique ultrices vel et nisl. ",
          image: "/img3.png",
          link: "https://example.com/post1",
        },
        {
          title: "Sed do eiusmod tempor incididunt",
          description:
            "Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          image: "/img3.png",
          link: "https://example.com/post2",
        },
        {
          title: "Duis aute irure dolor in reprehenderit",
          description:
            "Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident.",
          image: "/img3.png",
          link: "https://example.com/post3",
        },
      ],
    };
  },
};
</script>
