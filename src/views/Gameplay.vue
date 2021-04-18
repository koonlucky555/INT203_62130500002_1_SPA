<template>
  <div class="w-full h-screen bg-gray-100">
    <based-navbar />

    <!-- Gameplay -->
    <p class="text-4xl pt-28 flex justify-center text-black uppercase">
      My GamePlay
    </p>
    <p class="w3-center text-black pt-4">
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
      class="w3-container w3-content -mt-32"
      style="max-width: 800px"
      id="contact"
    >
      <h2 class="w3-wide w3-center uppercase text-2xl">comment</h2>
      <p class="w3-opacity w3-center"><i>Fan? Drop a note!</i></p>
      <p class="w3-opacity w3-center"><i>You can edit after submit next page.</i></p>
      <based-form/>
    </div>
  </div>
</template>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/MaterialDesign-Webfont/5.3.45/css/materialdesignicons.min.css");
</style>

<script>
import BasedForm from '../components/BasedForm.vue'
export default {
  components: {
    BasedForm
  }
  
};
</script>
