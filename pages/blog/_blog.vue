<template>
  <article v-if="blogPost" class="main article pt-5">
    <h1 class="article-title">{{ blogPost.title }}</h1>
    <h6
      v-if="blogPost.date"
      class="inline-block py-1 px-2 my-2 bg-accent text-white font-medium rounded-sm dark:bg-accent whitespace-no-wrap"
    >
      {{ formatDate(blogPost.date) }}
    </h6>
    <div v-html="$md.render(blogPost.body)" />
  </article>
</template>
<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload }
    else
      return {
        blogPost: await require(`~/assets/content/blog/${params.blog}.json`),
      }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
  },
  // Static metatag name
  // data() {
  //   return {
  //     title: 'Loremp ipsum metatag',
  //   }
  // },
  head() {
    return {
      title: this.title,
      // meta: [
      //   // hid is used as unique identifier. Do not use `vmid` for it as it will not work
      //   {
      //     hid: 'description',
      //     name: 'description',
      //     content: 'My custom description',
      //   },
      // ],
    }
  },
}
console.log(window)
</script>
