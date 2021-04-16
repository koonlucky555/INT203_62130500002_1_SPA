<template>
  <div class="w-full bg-white" id="tour">
    <div id="nav" class="absolute w-full p-12">
      <router-link to="/" class="text-black hover:text-gray-500 text-xl"
        >Home</router-link
      >
      <span class="text-black"> | </span>
      <router-link to="/about" class="text-black hover:text-gray-500 text-xl"
        >About Me</router-link
      >
      <span class="text-black"> | </span>
      <router-link to="/gameplay" class="text-black hover:text-gray-500 text-xl"
        >GamePlay</router-link
      >

      <span class="text-black"> | </span>
      <router-link to="/comment" class="text-black hover:text-gray-500 text-xl"
        >comment</router-link
      >
    </div>
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

    <div
      class="w3-container w3-content -mt-24"
      style="max-width: 800px"
      id="contact"
    >
      <h2 class="w3-wide w3-center uppercase text-2xl">comment</h2>
      <p class="w3-opacity w3-center"><i>Fan? Drop a note!</i></p>
      <div class="flex justify-center pt-10">
        <div class="w3-col m6">
          <form onsubmit="alert('give comment about me successfully!');return false">
            <div class="w3-row-padding" style="margin: 0 -16px 8px -16px">
              <div class="w3-half">
                <input
                  class="w3-input w3-border"
                  type="text"
                  placeholder="Name"
                  required
                  name="Name"
                />
              </div>
              <div class="w3-half">
                <input
                  class="w3-input w3-border"
                  type="text"
                  placeholder="Email"
                  required
                  name="Email"
                />
              </div>
            </div>
            <input
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
