<template lang="html">
  <div>
    <!-- This example requires Tailwind CSS v2.0+ -->
    <div class="pb-5">
      <h3 class="text-lg leading-6 font-medium text-gray-900">
        Selon-vous
      </h3>
      <p class="mt-2 max-w-4xl text-sm text-gray-500">La question précédente nous a permis de connaitre votr eniveau de compétence ?</p>
    </div>

    <fieldset class="mt-2">
      <legend class="sr-only">
        Privacy setting
      </legend>
      <div class="bg-white rounded-md -space-y-px">
        <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
        <label class="rounded-tl-md rounded-tr-md relative border p-4 flex cursor-pointer focus:outline-none">
          <input type="radio" name="privacy-setting" value="Public access" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="privacy-setting-0-label" aria-describedby="privacy-setting-0-description">
          <div class="ml-3 flex flex-col">
            <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
            <span id="privacy-setting-0-label" class="block text-sm font-medium">
              Oui
            </span>
          </div>
        </label>

        <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
        <label class="relative border p-4 flex cursor-pointer focus:outline-none">
          <input type="radio" name="privacy-setting" value="Private to Project Members" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="privacy-setting-1-label" aria-describedby="privacy-setting-1-description">
          <div class="ml-3 flex flex-col">
            <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
            <span id="privacy-setting-1-label" class="block text-sm font-medium">
              Non
            </span>
          </div>
        </label>

      </div>
    </fieldset>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
</style>
