<template>
  <div class="flex justify-center pt-6">
        <div class="w3-col m6">
          <form @submit.prevent="sendSubmit">
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
              type="submit"
            >
              SEND
            </button>
          </form>
        </div>
      </div>
</template>

<script>
import axios from 'axios'
export default {
 data() {
    return {
      name: null,
      email: null,
      message: null,
      formdata: [],
      Urlformdata: "http://localhost:5000/formdata",
      isEditting: false,
    };
  },
  methods: {
    sendSubmit() {
        axios
          .post(this.Urlformdata, {
            name: this.name,
            email: this.email,
            message: this.message,
          })
          .then((res) => {
            console.log(res);
            window.location.href = "/comment";
          });
      }
    },
}
</script>

