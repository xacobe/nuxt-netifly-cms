<template>
  <div class="main text-center flex flex-col items-center justify-center">
    <div class="grid grid-cols-1 gap-3 sm:grid-cols-2 lg:grid-cols-3 sm:px-8">
      <div class="w-full text-center sm:col-span-2 inset-x-0">
        <h1 class="title">Asociación do monte galego</h1>
        <h2 class="subtitle">Defendamos o bosque</h2>
        <p>
          Mollit enim voluptate consectetur irure. Sint adipisicing excepteur voluptate cupidatat ullamco laboris aliqua
          ullamco. Aute ea consequat commodo reprehenderit velit labore aliqua elit. Sunt occaecat nostrud ullamco
          voluptate minim cupidatat culpa velit esse ex cillum fugiat Lorem. Commodo duis sint ex minim esse sunt ea.
          Dolor et exercitation ullamco deserunt proident.
        </p>
      </div>
      <div class="p-2 text-center">
        <div class="py-16 rounded overflow-hidden shadow-lg hover:bg-white transition duration-500 bg-white">
          <div class="space-y-10">
            <font-awesome-icon icon="bacterium" class="w-6 mx-auto text-purple-800" />

            <div class="px-6 py-4">
              <div class="space-y-5">
                <div class="font-bold text-xl mb-2">Tempor irure.</div>
                <p class="text-gray-700 text-base">
                  Veniam proident voluptate sint cillum eiusmod ad pariatur qui adipisicing excepteur. Velit cillum aute
                  excepteur nostrud irure commodo nulla.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="p-2 text-center text-white">
        <div
          class="py-16 h-full rounded overflow-hidden shadow-lg bg-orange-500 hover:bg-orange-600 transition duration-500"
        >
          <div class="space-y-10">
            <font-awesome-icon icon="balance-scale-left" class="w-6 mx-auto" />
            <div class="px-6 py-4">
              <div class="space-y-5">
                <div class="font-bold text-xl mb-2">Magna incididunt.</div>
                <p class="text-base">
                  Commodo nulla non ut eu quis eiusmod irure laboris reprehenderit deserunt officia aliquip
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="sm:col-span-2 p-2 text-center translate-x-2">
        <div class="py-16 h-full rounded overflow-hidden shadow-lg hover:bg-white transition duration-500 bg-white">
          <div class="space-y-10">
            <font-awesome-icon icon="ban" class="w-6 mx-auto text-red-700" />
            <div class="px-6 py-4">
              <div class="space-y-5">
                <div class="font-bold text-xl mb-2">Duis officia sint.</div>
                <p class="text-gray-700 text-base">
                  Sint amet exercitation deserunt est reprehenderit id anim pariatur non fugiat ad do.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  // components: {
  //   Logo
  // },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    }
  },
}
</script>
