<template>
  <div class="w-full bg-white" id="tour">
    <based-navbar />
    <p class="text-4xl pt-20 flex justify-center text-black uppercase">
      All comment
    </p>
    <p class="w3-center text-black pt-8">
      <em>Here are some of comments<br /> </em>
    </p>
    <based-comment/>
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
