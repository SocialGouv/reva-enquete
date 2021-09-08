<template>
  <div class="p-8 flex justify-center">
    <div class="w-full h-full max-w-xl mx-auto pt-12 sm:pt-20">

      <div class="flex items-center justify-center">
        <nuxt-link to="/metier" class="ml-3 inline-flex items-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-gray-700 hover:bg-black focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
          Démarrer
        </nuxt-link>
        <div class="md:flex md:items-center py-12">
          <div class="mt-4 flex md:mt-0 md:ml-4">
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$parent.$emit('stepper', 0)
  }
}
</script>
