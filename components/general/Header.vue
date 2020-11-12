<template>
  <nav class="mx-auto">
    <img src="../../assets/img/asociacion-monte-galego.jpg" alt="Asociación do monte galego" />
    <ul class="flex 0 p-3">
      <li class="flex-1 mr-2">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1 mr-2">
        <nuxt-link class="btn block" to="/blog">Blog</nuxt-link>
      </li>
      <li class="flex-1">
        <nuxt-link class="btn block" to="/projects">Projects</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="postcss" scoped>
.nuxt-link-exact-active {
  @apply text-accent-100 bg-accent bg-opacity-20;
  &:hover {
    @apply text-white bg-accent-600;
  }
}
.light-mode {
  & .nuxt-link-exact-active {
    @apply text-accent-600;
    &:hover {
      @apply text-white;
    }
  }
}
</style>
