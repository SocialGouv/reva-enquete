<template>
  <div class="p-8 flex justify-center bg-white">
    <div class="w-full max-w-xl mx-auto pt-12 sm:pt-20">

      <Qone v-if="selectedQuestion == 1"/>
      <QonePonderate v-if="selectedQuestion == 2"/>
      <div class="" v-if="selectedQuestion == 3">
        seconde question
      </div>

      <div class="md:flex md:items-center md:justify-between py-12">
        <div class="flex-1 min-w-0">
          <button @click="decremente" type="button" class="inline-flex items-center px-4 py-2 border border-gray-300 rounded-md shadow-sm text-sm font-medium text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
            Question précédente
          </button>
        </div>
        <div class="mt-4 flex md:mt-0 md:ml-4">
          <button @click="incremente" type="button" class="ml-3 inline-flex items-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
            Question suivante
          </button>
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
