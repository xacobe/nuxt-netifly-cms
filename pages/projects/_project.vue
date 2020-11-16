<template>
  <article v-if="projectPost" class="main article">
    <img class="cover-image" :src="projectPost.cover" />
    <div class="px-6 py-4 bg-white">
      <h2 class="article-title text-3xl">{{ projectPost.title }}</h2>
      <p class="mt-4">{{ projectPost.description }}</p>
      <div class="block mt-8 mb-4 b-white" v-html="$md.render(projectPost.body)" />
    </div>
    <div v-if="projectPost.gallery">
      <img v-for="image in projectPost.gallery" class="image" :key="image.id" :src="image" />
    </div>
  </article>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { projectPost: payload }
    else
      return {
        projectPost: await require(`~/assets/content/projects/${params.project}.json`),
      }
  },
}
</script>