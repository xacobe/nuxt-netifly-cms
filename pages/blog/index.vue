<template>
  <main v-if="blogPosts" class="main">
    <h2 class="title text-left">Blog</h2>
    <ol class="grid gap-4 grid-cols-1 sm:gap-8 sm:grid-cols-2 lg:grid-cols-3">
      <li v-for="(blogPost, index) in blogPosts" :key="index" class="articles">
        <nuxt-link :to="`blog/${blogPost.slug}`" class="article article--clickable">
          <h3 class="article-title">{{ blogPost.title }}</h3>
          <h6
            v-if="blogPost.date"
            class="inline-block py-1 px-2 bg-accent text-white font-medium rounded-sm dark:bg-accent whitespace-no-wrap"
          >
            {{ formatDate(blogPost.date) }}
          </h6>
          <div class="mt-4 mb-2 font-light">
            <p class="inline">{{ blogPost.description }}</p>
          </div>
        </nuxt-link>
      </li>
    </ol>
  </main>
</template>
<script>
export default {
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    },
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
  },
}
</script>
