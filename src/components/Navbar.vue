<template>
  <header class="bg-white shadow-lg sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-2 relative">
    <div class="flex items-center justify-between px-4 py-3 sm:p-0">
      <div>
        <img class="h-16 " src="/img/tripantero-logo.jpg" alt="Logo" />

      </div>
      <div class="sm:hidden">
        <button
          @click="isOpen = !isOpen"
          type="button"
          class="block text-gray-500 focus:outline-none hover:bg-gray-200"
        >
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            <path
              v-if="isOpen"
              fill-rule="evenodd"
              d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
            />
            <path
              v-if="!isOpen"
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            />
          </svg>
        </button>
      </div>
    </div>
    <nav :class="isOpen ? 'block' : 'hidden'" class="px-2 pt-2 pb-4 sm:flex sm:p-0">
      <center>
      <a
        href="#"
        class="inline-block px-2 py-1 bg-green-500 text-white font-montserrat rounded hover:bg-green-400 hover:shadow-md focus:outline-none focus:shadow-outline active:bg-green-800 tracking-wider"
      >Add a Trip</a>
      </center>
    </nav>
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
