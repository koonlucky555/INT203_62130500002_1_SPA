<template>
  
  <div class="w-full bg-gray-100 h-screen" id="tour">
    <based-navbar />
    <p class="text-4xl flex justify-center pt-16 text-black uppercase">
      All comment
    </p>
    <p class="w3-center text-black pt-4">
      <em>Here are some of comments<br /> </em>
    </p>
    <div class="grid grid-cols-3">
      <based-comment />
    </div>
  </div>
</template>

<script>
import BasedComment from "../components/BasedComment.vue";
export default {
  components: {
    BasedComment,
  },
};
</script>
