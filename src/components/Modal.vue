<template>
  <div class="md:w-1/3 sm:w-full rounded-lg shadow-lg bg-white my-3" >
    <div class="flex justify-between border-b border-gray-100 px-5 py-4">
      <div>
        <i class="fa fa-exclamation-triangle text-orange-500"></i>
        <span class="font-bold text-gray-700 text-lg">Warning</span>
      </div>
      <div>
        <button>
          <i
            class="fa fa-times-circle text-red-500 hover:text-red-600 transition duration-150"
          ></i>
        </button>
      </div>
    </div>

    <div class="px-10 py-5 text-gray-600">
      Lorem ipsum dolor sit amet, consectetur adipi scing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua.
    </div>

    <div class="px-5 py-4 flex justify-end">
      <button
        class="bg-orange-500 mr-1 rounded text-sm py-2 px-3 text-white hover:bg-orange-600 transition duration-150"
      >
        Cancel
      </button>
      <button
        class="text-sm py-2 px-3 text-gray-500 hover:text-gray-600 transition duration-150"
      >
        OK
      </button>
    </div>
  </div>
</template>

<style scoped>
</style>

<script>
import BasedForm from "../components/BasedForm.vue";
export default {
  components: {
    BasedForm,
  },
};
</script>