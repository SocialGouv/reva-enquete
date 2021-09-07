<template>
  <div class="bg-yellow-100 relative">

    <section class="px-4 flex justify-center bg-white transition-opacity" v-bind:class="[displayEnqueteInterne ? 'opacity-50' : 'opacity-100']">
      <div class="w-full max-w-xl mx-auto pb-24 pt-6">

        <div class="pb-5">
          <h3 class="text-2xl leading-10 font-medium text-gray-900">
            Je suis sûr.e d'obtenir mon diplôme
          </h3>
          <!-- <p class="mt-2 max-w-4xl text-sm text-gray-500">Les pratiques et les savoir-faire sont aussi valorisables</p> -->
        </div>

        <fieldset class="mt-2">
          <legend class="sr-only">
            Pré-bilan
          </legend>
          <div class="bg-white rounded-md -space-y-px">

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-tl-md rounded-tr-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input v-on:change="changePreBilan" type="radio" v-model="preBilan" name="pre-bilan" value="0" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="pre-bilan-0-label" aria-describedby="pre-bilan-0-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="pre-bilan-0-label" class="block text-sm font-medium">
                  Pas du tout d'accord
                </span>
                <!-- Checked: "text-indigo-700", Not Checked: "text-gray-500" -->
                <!-- <span id="pre-bilan-0-description" class="block text-sm text-gray-500">
                  Je n'ai pas du tout exercé de métier en lien avec le diplôme
                </span> -->
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="relative border p-4 flex cursor-pointer focus:outline-none">
              <input v-on:change="changePreBilan" type="radio" v-model="preBilan" name="pre-bilan" value="1" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="pre-bilan-1-label" aria-describedby="pre-bilan-1-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="pre-bilan-1-label" class="block text-sm font-medium">
                  Pas d'accord
                </span>
                <!-- Checked: "text-indigo-700", Not Checked: "text-gray-500" -->
                <!-- <span id="pre-bilan-1-description" class="block text-sm text-gray-500">
                  J'ai exercé un métier en partie ou similaire au diplôme
                </span> -->
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input v-on:change="changePreBilan" type="radio" v-model="preBilan" name="pre-bilan" value="2" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="pre-bilan-2-label" aria-describedby="pre-bilan-2-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="pre-bilan-2-label" class="block text-sm font-medium">
                  Ni d'accord, ni pas d'accord
                </span>
                <!-- Checked: "text-indigo-700", Not Checked: "text-gray-500" -->
                <!-- <span id="pre-bilan-2-description" class="block text-sm text-gray-500">
                  J'ai exercé un métier en lien avec le diplôme peu de temps mais suffisament pour valider mes compétences
                </span> -->
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input v-on:change="changePreBilan" type="radio" v-model="preBilan" name="pre-bilan" value="3" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="pre-bilan-3-label" aria-describedby="pre-bilan-3-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="pre-bilan-3-label" class="block text-sm font-medium">
                  Plutôt d'accord
                </span>
                <!-- Checked: "text-indigo-700", Not Checked: "text-gray-500" -->
                <!-- <span id="pre-bilan-3-description" class="block text-sm text-gray-500">
                  J'ai exercé un métier en lien avec le diplôme suffisament de temps
                </span> -->
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input v-on:change="changePreBilan" type="radio" v-model="preBilan" name="pre-bilan" value="4" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="pre-bilan-4-label" aria-describedby="pre-bilan-4-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="pre-bilan-4-label" class="block text-sm font-medium">
                  Complètement d'accord
                </span>
                <!-- Checked: "text-indigo-700", Not Checked: "text-gray-500" -->
                <!-- <span id="pre-bilan-4-description" class="block text-sm text-gray-500">
                  J'ai exercé plusieurs métiers fortement liés au diplôme
                </span> -->
              </div>
            </label>

          </div>
        </fieldset>

      </div>
    </section>

    <section class="px-4 flex justify-center bg-yellow-100 transition-all transform" v-bind:class="[displayEnqueteInterne ? 'absolute sm:relative bottom-0 sm:-translate-y-80' : 'hidden translate-y-0']">
      <div class="w-full max-w-xl mx-auto pt-8">
        <div class="pb-5">
          <p class="mt-2 max-w-4xl text-xl text-gray-800">
            Selon vous, la question ci-dessus permet de mesurer ma confiance en mon obtention du diplôme
          </p>
        </div>

        <fieldset class="mt-2">
          <legend class="sr-only">
            Enquête interne
          </legend>
          <div class="bg-white rounded-md -space-y-px">

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label @click="more" class="rounded-tl-md rounded-tr-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input type="radio" name="enquete-interne" value="0" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="enquete-interne-0-label" aria-describedby="enquete-interne-0-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="enquete-interne-0-label" class="block text-sm font-medium">
                  Pas du tout d'accord
                </span>
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label @click="more" class="relative border p-4 flex cursor-pointer focus:outline-none">
              <input type="radio" name="enquete-interne" value="1" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="enquete-interne-1-label" aria-describedby="enquete-interne-1-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="enquete-interne-1-label" class="block text-sm font-medium">
                  Pas d'accord
                </span>
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label @click="more" class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input type="radio" name="enquete-interne" value="3" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="enquete-interne-2-label" aria-describedby="enquete-interne-2-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="enquete-interne-2-label" class="block text-sm font-medium">
                  Ni d'accord, ni pas d'accord
                </span>
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input type="radio" name="enquete-interne" value="4" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="enquete-interne-3-label" aria-describedby="enquete-interne-3-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="enquete-interne-3-label" class="block text-sm font-medium">
                  Plutôt d'accord
                </span>
              </div>
            </label>

            <!-- Checked: "bg-indigo-50 border-indigo-200 z-10", Not Checked: "border-gray-200" -->
            <label class="rounded-bl-md rounded-br-md relative border p-4 flex cursor-pointer focus:outline-none">
              <input type="radio" name="enquete-interne" value="5" class="h-4 w-4 mt-0.5 cursor-pointer text-indigo-600 border-gray-300 focus:ring-indigo-500" aria-labelledby="enquete-interne-4-label" aria-describedby="enquete-interne-4-description">
              <div class="ml-3 flex flex-col">
                <!-- Checked: "text-indigo-900", Not Checked: "text-gray-900" -->
                <span id="enquete-interne-4-label" class="block text-sm font-medium">
                  Complètement d'accord
                </span>
              </div>
            </label>

          </div>
          <div v-if="displayMore" class="mt-4">
            <label for="about" class="block text-sm font-medium sm:mt-px sm:pt-2">
              Pouvez-vous compléter votre choix ?
            </label>
            <div class="mt-1 sm:mt-0 sm:col-span-2">
              <textarea id="about" name="about" rows="5" class="block w-full focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm border border-gray-300 rounded-md"></textarea>
            </div>
          </div>
        </fieldset>

        <div class="md:flex md:items-center md:justify-between py-12">
          <div class="flex-1 min-w-0">
            <nuxt-link to="confiance_choix" type="button" class="inline-flex items-center px-4 py-2 border border-gray-300 rounded-md shadow-sm text-sm font-medium text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
              Question précédente
            </nuxt-link>
          </div>
          <div class="mt-4 flex md:mt-0 md:ml-4">
            <nuxt-link to="disponibilite" type="button" class="ml-3 inline-flex items-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-gray-700 hover:bg-black focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
              Question suivante
            </nuxt-link>
          </div>
        </div>

      </div>
    </section>

  </div>
</template>

<script>
export default {
  data() {
    return {
      preBilan: null,
      enqueteInterne: null,
      displayEnqueteInterne: false,
      displayMore: false,
    }
  },
  methods: {
    changePreBilan () {
      this.displayEnqueteInterne = !this.displayEnqueteInterne
    },
    nextPage () {
      // goto
    },
    previousPage () {
      // goto
    },
    more() {
      this.displayMore = true
    }
  }
}
</script>
