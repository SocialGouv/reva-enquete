<template>
  <div class="antialiased">
    <!-- Stepper desktop -->
    <nav class="hidden md:block py-12" aria-label="Progression">
      <ol role="list" class="flex items-center justify-center">
        <li class="relative pr-8 lg:pr-20">
          <!-- Completed Step -->
          <!-- <div class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-indigo-600"></div>
          </div> -->
          <div class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 1 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <!-- Heroicon name: solid/check -->
            <!-- <svg class="w-5 h-5 text-white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
              <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
            </svg> -->
            <span v-if="current === 1" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 1</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <div v-if="current === 2" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 2 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 2" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 2</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <!-- Current Step -->
          <div v-if="current === 3" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 3 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 3" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 3</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <!-- Upcoming Step -->
          <div v-if="current === 4" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 4 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 4" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 4</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <div v-if="current === 5" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 5 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 5" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 4</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <div v-if="current === 6" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 6 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 6" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 4</span>
          </div>
        </li>

        <li class="relative pr-8 lg:pr-20">
          <div v-if="current === 7" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 7 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 7" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 4</span>
          </div>
        </li>

        <li class="relative">
          <div v-if="current === 8" class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-else class="absolute inset-0 flex items-center" aria-hidden="true">
            <div class="h-0.5 w-full bg-gray-200"></div>
          </div>
          <div v-bind:class="[current === 8 ? 'border-indigo-600' : 'border-gray-300 hover:border-gray-400']" class="relative w-8 h-8 flex items-center justify-center bg-white border-2 rounded-full">
            <span v-if="current === 8" class="h-2.5 w-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span v-else class="h-2.5 w-2.5 bg-transparent rounded-full group-hover:bg-gray-300" aria-hidden="true"></span>
            <span class="sr-only">Step 5</span>
          </div>
        </li>
      </ol>
    </nav>

    <!-- Stepper mobile -->
    <nav class="block md:hidden py-12 flex items-center justify-center" aria-label="Progression">
      <!-- <p class="text-sm font-medium">Step 2 of 4</p> -->
      <ol role="list" class="ml-8 flex items-center space-x-5">
        <li>
          <!-- Completed Step -->
          <a href="#" class="block w-2.5 h-2.5 bg-indigo-600 rounded-full hover:bg-indigo-900">
            <span class="sr-only">Step 1</span>
          </a>
        </li>

        <li>
          <!-- Current Step -->
          <a href="#" class="relative flex items-center justify-center" aria-current="step">
            <span class="absolute w-5 h-5 p-px flex" aria-hidden="true">
              <span class="w-full h-full rounded-full bg-indigo-200"></span>
            </span>
            <span class="relative block w-2.5 h-2.5 bg-indigo-600 rounded-full" aria-hidden="true"></span>
            <span class="sr-only">Step 2</span>
          </a>
        </li>

        <li>
          <!-- Upcoming Step -->
          <a href="#" class="block w-2.5 h-2.5 bg-gray-200 rounded-full hover:bg-gray-400">
            <span class="sr-only">Step 3</span>
          </a>
        </li>

        <li>
          <!-- Upcoming Step -->
          <a href="#" class="block w-2.5 h-2.5 bg-gray-200 rounded-full hover:bg-gray-400">
            <span class="sr-only">Step 4</span>
          </a>
        </li>
      </ol>
    </nav>

    <div id="app">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: null,
    }
  },
  mounted() {
    this.$nuxt.$on('stepper', (e) => {
      this.current = e
    })
  }
}
</script>
