<template>
  <div class="w-full bg-white">
    <based-navbar />

    <!-- Gameplay -->
    <p class="text-4xl pt-20 flex justify-center text-black uppercase">
      My GamePlay
    </p>
    <p class="w3-center text-black pt-8">
      <em
        >Here are some of my latest gameplay.<br />
        Click on the picture to go to the original game website.
      </em>
    </p>
    <br />
    <div class="grid grid-cols-3 p-32 justify-items-center pt-2">
      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a href="https://www.ea.com/games/apex-legends"
          ><img
            src="../assets/apex1.jpg"
            alt="Apex"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container bg-white">
          <p class="text-black text-lg pb-8"><b>Apex</b></p>
        </div>
      </div>

      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a href="https://playvalorant.com/th-th/"
          ><img
            src="../assets/valorant.jpg"
            alt="Valorant"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container w3-white">
          <p class="text-black text-lg pb-8"><b>Valorant</b></p>
        </div>
      </div>

      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a
          href="https://store.steampowered.com/app/346110/ARK_Survival_Evolved/"
          ><img
            src="../assets/ark.jpg"
            alt="Ark"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container w3-white">
          <p class="text-black text-lg pb-8"><b>Ark</b></p>
        </div>
      </div>

      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a href="https://pointblank.zepetto.com/th/"
          ><img
            src="../assets/PB.jpg"
            alt="PointBlank"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container bg-white">
          <p class="text-black text-lg pb-8"><b>PointBlank</b></p>
        </div>
      </div>

      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a href="https://www.pubgmobile.com/th/home.shtml"
          ><img
            src="../assets/pubgM.jpg"
            alt="PUBG M"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container bg-white">
          <p class="text-black text-lg pb-8"><b>Pubg Moblie</b></p>
        </div>
      </div>

      <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
        <a href="https://fallguys.com/"
          ><img
            src="../assets/fallguys.jpg"
            alt="Fall Guys"
            style="width: 100%"
            class="w3-hover-opacity"
        /></a>
        <div class="w3-container pb-8 bg-white">
          <p class="text-black text-lg"><b>Fall Guys</b></p>
        </div>
      </div>
    </div>

    <!-- Comment -->
    <div
      class="w3-container w3-content -mt-24"
      style="max-width: 800px"
      id="contact"
    >
      <h2 class="w3-wide w3-center uppercase text-2xl">comment</h2>
      <p class="w3-opacity w3-center"><i>Fan? Drop a note!</i></p>
      <div class="flex justify-center pt-10">
        <div class="w3-col m6">
          <form @submit.prevent="sendSubmit">
            <div class="w3-row-padding" style="margin: 0 -16px 8px -16px">
              <div class="w3-half">
                <input v-model="name"
                  class="w3-input w3-border"
                  type="text"
                  placeholder="Name"
                  required
                  name="Name"
                />
              </div>
              <div class="w3-half">
                <input v-model="email"
                  class="w3-input w3-border"
                  type="text"
                  placeholder="Email"
                  required
                  name="Email"
                  pattern="[a-z0-9._%+-]+@[a-z0-9.-]+.[a-z]{2,}$"
                />
              </div>
            </div>
            <input v-model="message"
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
    </div>
  </div>
</template>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/MaterialDesign-Webfont/5.3.45/css/materialdesignicons.min.css");
</style>

<script>
import axios from "axios";
export default {
 
  data() {
    return {
      name: null,
      email: null,
      message: null,
      formdata: [

      ],
      Urlformdata: 'http://localhost:5000/formdata'
    };
  },
  methods: {
    sendSubmit() {
      axios.post(this.Urlformdata , {
        name: this.name,
        email: this.email,
        message: this.message
      }
      ).then(res => {
        console.log(res);
        window.location.href = '/comment'
      });
    },
  },
};
</script>
