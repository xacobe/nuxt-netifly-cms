<template>
  <main class="container">
    <section v-if="projectPosts" class="main">
      <h1 class="title text-left pb-2 text-gray-800">Projects</h1>
      <ol>
        <li
          v-for="(projectPost, index) in projectPosts"
          :key="index"
          class="articles flex mx-auto bg-white overflow-hidden shadow-md mb-6"
        >
          <nuxt-link class="article article--clickable" :to="`projects/${projectPost.slug}`">
            <div class="flex flex-row">
              <div class="w-1/2 md:w-1/2">
                <img class="w-full h-full object-cover flex-1" :src="projectPost.cover" alt="Article" />
              </div>
              <div class="w-2/3 md:w-1/2 pl-6">
                <span class="text-blue-600 text-xs font-medium uppercase">{{ projectPost.project_type }}</span>
                <a
                  href="#"
                  class="block text-gray-800 font-semibold text-2xl mt-2 hover:text-gray-600 hover:underline"
                  >{{ projectPost.title }}</a
                >
                <p class="text-sm text-gray-600 mt-2">
                  {{ projectPost.description }}
                </p>
              </div>
            </div>
          </nuxt-link>
        </li>
      </ol>
    </section>
  </main>
</template>
<script>
export default {
  computed: {
    projectPosts() {
      return this.$store.state.projectPosts
    },
  },
}
</script>
