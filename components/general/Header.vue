<template>
  <header class="bg-green text-white w-full top-0 left-0">
    <nav class="main-menu bg-gray-100 hidden sm:block">
      <ul class="flex text-base sm:text-lg px-8 py-4 justify-end uppercase">
        <li>
          <nuxt-link to="/" class="mr-4"> Inicio </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/blog" class="mr-4"> Noticias </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/projects" class=""> Proyectos </nuxt-link>
        </li>
      </ul>
    </nav>

    <!-- Toggle menu mobile icon -->
    <div class="sm:hidden absolute px-8 py-4 right-0" @click="menu = !menu">
      <font-awesome-icon icon="bars" style="font-size: 2rem" />
    </div>

    <!-- Logo -->
    <div class="logo w-16 sm:w-24 mx-8 my-4">
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

    <!-- Mobile nav list -->
    <nav v-show="menu" class="mobile-menu w-full bg-white text-center text-lg uppercase">
      <ul class="flex flex-col">
        <li v-for="(item, index) in items" :key="index">
          <a :href="item.href" class="p-6 block">
            {{ item.title }}
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      menu: false,
      items: [
        {
          title: 'Inicio',
          href: '/',
        },
        {
          title: 'Noticias',
          href: '/blog',
        },
        {
          title: 'Proyectos',
          href: '/projects',
        },
      ],
    }
  },
}
</script>

<style lang="postcss" scoped>
.nuxt-link-exact-active {
  @apply text-green-100 border-b-8 border-primary-900;
}
.mobile-menu li a {
  position: relative;
  border-bottom: solid 1px darkgrey;
  overflow: hidden;

  &:hover,
  &:focus {
    @apply bg-blue-100 underline;
  }

  &:focus-within {
    background: #c9ecff;
    @apply flex justify-center;
    &::before {
      content: '';
      display: block;
      width: 1px;
      height: 1px;
      background: rgb(124, 170, 255);
      opacity: 0;
      border-radius: 100%;
      position: absolute;
      animation: circlepop 1s forwards;
    }
  }
}
@keyframes circlepop {
  from {
    opacity: 1;
    transform: scale(0);
    transform-origin: center;
  }
  to {
    opacity: 0;
    transform: scale(500);
    transform-origin: center;
  }
}
.light-mode {
  & .nuxt-link-exact-active {
    @apply text-primary-900;
  }
}
</style>
