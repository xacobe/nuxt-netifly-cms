<template>
  <div class="wrapper bg-primary-100 w-full">
    <Header />
    <Breadcrumb />
    <ColorModePicker />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/general/Header.vue'
import Breadcrumb from '~/components/general/Breadcrumb.vue'
import ColorModePicker from '~/components/general/ColorModePicker.vue'
import Footer from '~/components/general/Footer.vue'

export default {
  components: {
    Header,
    Breadcrumb,
    ColorModePicker,
    Footer,
  },
}
</script>
