<template>
  <header class="bg-teal-900 shadow-xl sm:flex sm:justify-between sm:px-4 sm:py-3">
    <div class="container sm:flex items-center sm:justify-between mx-auto">
      <nav
        class="flex items-center justify-between px-4 py-2 border-b border-gray-700 sm:p-0 sm:border-none"
      >
        <div>
          <h1 class="text-gray-200 font-sans text-2xl">
            <a href="#"> <span class="text-teal-400">Am</span>kam</a>
          </h1>
        </div>
        <div class="sm:hidden">
          <button
            @click="isOpen = !isOpen"
            type="button"
            class="text-teal-400 focus:text-white focus:outline-none hover:text-white block"
          >
            <svg
              class="h-6 w-6 fill-current"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path v-if="isOpen" d="M6 18L18 6M6 6l12 12" />
              <path v-if="!isOpen" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </nav>

      <div :class="isOpen ? 'block' : 'hidden' " class="px-2 pt-2 pb-4 sm:flex sm:p-0 sm:pt-1">
        <a
          href="/"
          class="block sm:inline-block text-white font-semibold hover:bg-teal-800 rounded px-2 py-1"
        >Home</a>
        <a
          href="#"
          class="block sm:inline-block text-white font-semibold hover:bg-teal-800 rounded px-2 py-1 mt-1 sm:mt-0 sm:ml-3"
        >About</a>
        <a
          href="#"
          class="block sm:inline-block text-white font-semibold hover:bg-teal-800 rounded px-2 py-1 mt-1 sm:mt-0 sm:ml-3"
        >Portfolio</a>
        <a
          href="#"
          class="block sm:inline-block text-white font-semibold hover:bg-teal-800 rounded px-2 py-1 mt-1 sm:mt-0 sm:ml-3"
        >Contact</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  }
};
</script>