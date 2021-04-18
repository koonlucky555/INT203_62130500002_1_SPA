<template>
  <div class="pt-24 p-20 justify-items-center">
    <div
      class="rounded overflow-hidden shadow-lg bg-white py-4 px-4"
      @click="emitComment(comment) "
    >
      <img
        src="../assets/user.png"
        alt="Avatar"
        class="w3-left w3-circle w3-margin-right"
        style="width: 80px"
      />
      <p>
        <span class="text-xl pr-4">{{ comment.name }}</span>
        <span class="text-sm opacity-70">{{ comment.email }}</span>
      </p>
      <p class="pt-2">{{ comment.message }}</p>
      <br />
    </div>
    </div>
</template>

<script>
export default {
  props: ["comment"],
  modals: Object,
  mounted() {
    console.log(this.comment);
  },
  name: "SingleComment",
  methods: {
    emitComment(comment) {
      this.$router.push({ name: "Modal", params: { id: comment.id } });
    },
  },
};
</script>

