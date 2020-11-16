<template>
  <header class="bg-green text-white w-full top-0 left-0">
    <nav class="main-menu bg-gray-100 hidden sm:block">
      <ul class="flex text-base sm:text-lg px-8 py-4 justify-end uppercase">
        <li class="hover:text-red-600">
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
    <div class="sm:hidden absolute px-8 py-4 right-0 cursor-pointer" @click="menu = !menu">
      <font-awesome-icon icon="bars" style="font-size: 2rem" />
    </div>

    <!-- Branding -->
    <section class="container">
      <div class="logo w-64 mx-8 my-4">
        <a href="/">
          <img
            title="Asocicación do monte galego"
            src="../../assets/img/logo_mobile.svg"
            alt="Asociacion do monte
        galego"
          />
        </a>
      </div>
    </section>

    <!-- Mobile nav list -->
    <nav v-show="menu" class="mobile-menu w-full bg-white transition-all text-center text-lg uppercase">
      <ul class="flex flex-col">
        <li v-for="(item, index) in items" :key="index" :value="item.href">
          <nuxt-link :to="item.href" class="p-6 block">
            {{ item.title }}
          </nuxt-link>
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
/* Main menu. */
.main-menu li a {
  &:hover,
  &:focus {
    border-bottom: solid 0.2em #74d14d;
    padding-bottom: 0.35rem;
    transition: none;
  }
  &.nuxt-link-exact-active {
    border-bottom: solid 0.2em #74d14d;
    padding-bottom: 0.35rem;
  }
}

/* Mobile men. */
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
/* Light mode. */
.light-mode {
  & .nuxt-link-exact-active {
    @apply text-primary-900;
  }
}
</style>
