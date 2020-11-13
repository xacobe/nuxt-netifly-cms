<template>
  <div class="container">
    <div class="wrapper bg-primary-100 shadow-2xl w-full mt-12">
      <Header />
      <ColorModePicker />
      <nuxt />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from '~/components/general/Header.vue'
import ColorModePicker from '~/components/general/ColorModePicker.vue'
import Footer from '~/components/general/Footer.vue'

export default {
  components: {
    Header,
    ColorModePicker,
    Footer,
  },
}
</script>
