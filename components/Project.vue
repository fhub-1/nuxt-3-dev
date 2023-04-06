<template>
  <section class="bg-primary text-white px-5 py-32" id="projects">
    <div
      class="container mx-auto grid md:grid-cols-2 items-center md:justify-between"
    >
      <div class="about-info mb-5">
        <h2
          class="text-4xl font-bold mb-5 border-b-[5px] w-[180px] border-yellow-600 pb-2"
        >
          Projects
        </h2>
        <p class="pb-5">
          These are some of my best projects. I have built these with React,
          MERN and vanilla CSS. Check them out.
        </p>
      </div>
    </div>

    <div class="projects container mx-auto grid md:grid-cols-3 gap-10">
      <div v-for="(project, i) in projects" :key="i" class="relative">
        <img :src="project.img" :alt="project.title" />
        <div
          class="flex absolute left-0 right-0 top-[13px] bottom-0 mx-auto w-[90%] h-[90%] bg-primary opacity-0 duration-500 justify-center flex-col hover:opacity-100"
        >
          <p class="py-5 text-center font-bold px-2 text-white">
            {{ project.desc }}
          </p>
          <div class="mx-auto">
            <a
              :href="project.live"
              class="px-5 py-2 bg-yellow-500 hover:bg-yellow-600 mr-5 font-bold"
              >Live</a
            >
            <a
              :href="project.code"
              class="px-5 py-2 bg-yellow-700 hover:bg-yellow-800 font-bold"
              >Code</a
            >
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
      projects: [
        {
          img: "/img3.png",
          title: "Project 1",
          desc: "This is the description of Project 1.",
          live: "https://example.com",
          code: "https://github.com/example/project-1",
        },
        {
          img: "/img3.png",
          title: "Project 2",
          desc: "This is the description of Project 2.",
          live: "https://example.com",
          code: "https://github.com/example/project-2",
        },
        {
          img: "/img3.png",
          title: "Project 3",
          desc: "This is the description of Project 3.",
          live: "https://example.com",
          code: "https://github.com/example/project-3",
        },
      ],
    };
  },
};
</script>
