<template>
  <div class="h-screen w-full bg-gray-100">
    <p class="text-4xl pt-20 flex justify-center text-black uppercase">
      Edit & Delete
    </p>
    <div class="flex justify-center pt-6">
      <div class="w3-col m6" @submit.prevent="">
        <form>
          <div class="w3-row-padding" style="margin: 0 -16px 8px -16px">
            <div class="w3-half">
              <input
                v-model="name"
                class="w3-input w3-border"
                type="text"
                placeholder="Name"
                required
                name="Name"
              />
            </div>
            <div class="w3-half">
              <input
                v-model="email"
                class="w3-input w3-border"
                type="text"
                placeholder="Email"
                required
                name="Email"
                pattern="[a-z0-9._%+-]+@[a-z0-9.-]+.[a-z]{2,}$"
              />
            </div>
          </div>
          <input
            v-model="message"
            class="w3-input w3-border"
            type="text"
            placeholder="Message"
            required
            name="Message"
          />
          <button
            class="w3-button w3-black w3-section w3-right"
            @click="editComment"
          >
            Edit
          </button>
          <button
            class="w3-button w3-black w3-section w3-righ"
            @click="deleteComment"
          >
            Delete</button
          ><br />
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ["id"],
  data() {
    return {
      name: "",
      email: "",
      message: "",
      url: "http://localhost:8081/comment/" + this.id,
      checkComment: [],
      readyToConfirm: false,
    };
  },
  methods: {
    backToPageComment() {
      this.$router.push("/comment");
    },
    async editComment() {
      if (this.readyToConfirm) {
        let editData = {
          name: this.name,
          email: this.email,
          meassage: this.message,
        };
        await fetch(this.url, {
          method: "PUT",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(editData),
        });
        this.$router.push("/comment");
      }
    },
    async deleteComment() {
      if (this.readyToConfirm) {
        await fetch(this.url, {
          method: "DELETE",
        });
        this.$router.push("/comment");
      }
    },
    async mounted() {
      const res = await fetch(this.url);
      const data = await res.json();
      this.checkComment = data;
      this.name = data.name;
      this.email = data.email;
      this.message = data.message;
    },
  },
};
</script>