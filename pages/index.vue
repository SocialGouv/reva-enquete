<template>
  <div class="p-8 flex justify-center bg-yellow-100">
    <div class="w-full max-w-xl mx-auto pt-12 sm:pt-20">

      <div class="md:flex md:items-center md:justify-between py-12">
        <div class="flex-1 min-w-0">
        </div>
        <div class="mt-4 flex md:mt-0 md:ml-4">
          <nuxt-link to="/metier" class="ml-3 inline-flex items-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-gray-700 hover:bg-black focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
            Démarrer
          </nuxt-link>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedQuestion: 1
    }
  },
  methods: {
    incremente () {
      this.selectedQuestion++
    },
    decremente() {
      this.selectedQuestion--
    }
  }
}
</script>
