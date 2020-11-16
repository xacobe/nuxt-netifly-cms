<template>
  <main v-if="projectPosts" class="main">
    <h1 class="title text-left text-gray-800">Projects</h1>
    <ol>
      <!-- <li v-for="(projectPost, index) in projectPosts" :key="index" class="articles">
        <nuxt-link class="article article--clickable" :to="`projects/${projectPost.slug}`">
          <h3 class="article-title">{{ projectPost.title }}</h3>
          <div class="mt-4 mb-2">
            <h2 class="inline py-1 px-2 mr-1 bg-accent text-white font-medium rounded-sm dark:bg-accent">
              {{ projectPost.project_type }}
            </h2>
            <p class="inline">{{ projectPost.description }}</p>
          </div>
        </nuxt-link>
      </li> -->
      <li
        v-for="(projectPost, index) in projectPosts"
        :key="index"
        class="articles flex mx-auto bg-white overflow-hidden shadow-md"
      >
        <nuxt-link class="article article--clickable flex flex-row" :to="`projects/${projectPost.slug}`">
          <div class="w-1/2">
            <img
              class="w-full h-full object-cover flex-1"
              src="https://images.unsplash.com/photo-1550439062-609e1531270e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60"
              alt="Article"
            />
          </div>

          <div class="p-6">
            <div>
              <span class="text-blue-600 text-xs font-medium uppercase">{{ projectPost.project_type }}</span>
              <a href="#" class="block text-gray-800 font-semibold text-2xl mt-2 hover:text-gray-600 hover:underline">{{
                projectPost.title
              }}</a>
              <p class="text-sm text-gray-600 mt-2">
                {{ projectPost.description }}
              </p>
            </div>
          </div>
        </nuxt-link>
      </li>
    </ol>
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
