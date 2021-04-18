<template>
  <div class="w-full bg-gray-900 " id="tour">
    <based-navbar />
    <div class="bg-gray-900 h-screen">
    <p class="text-4xl flex justify-center pt-28 text-white uppercase">
      All comment
    </p>
    <p class="w3-center text-white pt-4">
      <em>Here are some of comments<br /> </em>
      <em>You can edit or delete.. Click it !<br /> </em>
    </p>
    
    <div class="grid grid-cols-3">
      <based-comment />
    </div>
</div>
    <!-- Modal-->
    <form-click @when-click="switchModal" :modals="modal"></form-click>
      
  </div>
</template>

<script>
import BasedComment from "../components/BasedComment.vue";
export default {
  components: {
    BasedComment,
  },
  modal: {
 
  },
  methods: {

  },
};
</script>


