<template>
  <header class="bg-green text-white w-full top-0 left-0 p-8">
    <div class="sm:mx-auto flex flex-wrap justify-between">
      <div class="logo w-16 sm:w-24">
        <a href="/">
          <img
            class="w-full"
            src="../../assets/img/logo.svg"
            alt="Asociación do monte galego"
            width="100px"
            height="132.15"
          />
        </a>
      </div>
      <div class="flex flex-wrap">
        <!-- Desktop nav list -->
        <nav>
          <ul id="mobileMenu" class="text-md sm:text-xl flex uppercase">
            <li>
              <nuxt-link to="/" class="mr-4"> Inicio </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/blog" class="mr-4"> Blog </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/projects" class=""> Projects </nuxt-link>
            </li>
          </ul>
        </nav>
        <!-- Toggle menu mobile icon -->
        <!-- <div class="ml-auto sm:hidden" @click="menu = !menu">
          <font-awesome-icon icon="bars" style="font-size: 2rem" />
        </div> -->
        <!-- Mobile nav list -->
        <!-- <nav v-show="menu" class="w-full">
          <ul class="flex flex-col text-center">
            <li v-for="(item, index) in items" :key="index">
              <a :href="item.href" class="hover:bg-green-500 p-6 block">
                {{ item.title }}
              </a>
            </li>
          </ul>
        </nav> -->
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  // data() {
  //   return {
  //     menu: false,
  //     items: [
  //       {
  //         title: 'Home',
  //         href: '/',
  //       },
  //       {
  //         title: 'Blog',
  //         href: '/blog',
  //       },
  //       {
  //         title: 'Projects',
  //         href: '/projects',
  //       },
  //     ],
  //   }
  // },
}
</script>

<style lang="postcss" scoped>
.nuxt-link-exact-active {
  @apply text-green-100 border-b-8 border-primary-900;
  &:hover {
    @apply text-white;
  }
}
.light-mode {
  & .nuxt-link-exact-active {
    @apply text-primary-900;
    &:hover {
      @apply text-white;
    }
  }
}
</style>
