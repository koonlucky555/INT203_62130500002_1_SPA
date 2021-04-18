<template>
<based-navbar />
  <div class="h-screen w-full bg-gray-100">
    <p class="text-4xl pt-36 flex justify-center text-black uppercase">
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
            class="w3-button w3-black w3-section w3-left"
            @click="editComment"
          >
            Edit
          </button>
          <button
            class="w3-button bg-red-600 text-white hover:bg-gray-400 hover:text-black w3-section w3-right "
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
import axios from 'axios'
export default {
  name: "Modal",
  props: ["id"],
  data() {
    return {
      name: "",
      email: "",
      message: "",
      url: "http://localhost:5000/formdata/" + this.id,
      checkComment: {},
      readyToConfirm: false,
    };
  },
  methods: {

    backToPageComment() {
      this.$router.push("/comment");
    },

    editComment(){
      
      axios.put(this.url,{
        name: this.name,
          email: this.email,
          message: this.message,
      }).then(res => {
            console.log(res)
            this.$router.push("/comment");
      })

    },

     deleteComment() {
        axios.delete(this.url).then(res => {
            console.log(res)
            this.$router.push("/comment");
      })
      
    },
    async getData() {
      try {
        const response = await fetch(this.url);
        const data = await response.json();
        return data;
      } catch (error) {
        console.log(error);
      }
    },

  },
  async created(){
    this.checkComment = await this.getData();
      this.name = this.checkComment.name;
      this.email = this.checkComment.email;
      this.message = this.checkComment.message;
    console.log(this.checkComment);
  }
};
</script>