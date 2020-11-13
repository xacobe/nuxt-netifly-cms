<template>
  <footer class="footer flex justify-center w-full p-4 bg-gray-900">
    <div class="footer-content flex">
      <a href="/" class="icon-link flex flex-col px-5" title=""
        ><font-awesome-icon
          :icon="['fab', 'twitter']"
          class="icon-twitter p-3 bg-gray-600 rounded-full"
          style="font-size: 60px"
        />
        <p class="text-primary-400 pt-2">Email</p></a
      >
      <a href="/" class="icon-link flex flex-col px-5" title=""
        ><font-awesome-icon
          :icon="['fab', 'facebook']"
          class="icon-facebook fill-current text-gray-600 rounded-full"
          style="font-size: 60px"
        />
        <p class="text-primary-400 pt-2">Email</p></a
      >
      <a href="/" class="icon-link flex flex-col px-5" title=""
        ><font-awesome-icon icon="at" class="icon-at p-2 bg-gray-600 rounded-full" style="font-size: 60px" />
        <p class="text-primary-400 pt-2">Email</p></a
      >
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="postcss" scoped>
.icon-twitter {
  &:hover {
    color: #fff;
    background: #1da1f2;
  }
}
.icon-facebook {
  &:hover {
    color: #38529a;
    background: #fff;
  }
}
.icon-at {
  &:hover {
    color: #fff;
    background: grey;
  }
}
</style>