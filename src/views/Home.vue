<template>
  <div class="home">
    <div id="nav" class="absolute w-full p-12">
      <router-link to="/" class="text-white hover:text-black text-xl"
        >Home</router-link
      >
      <span class="text-white"> | </span>
      <router-link to="/about" class="text-white hover:text-black text-xl"
        >About Me</router-link
      >
      <span class="text-white"> | </span
      ><router-link to="/gameplay" class="text-white hover:text-black text-xl"
        >GamePlay</router-link
      >

      <span class="text-white"> | </span>
      <router-link to="/comment" class="text-white hover:text-black text-xl"
        >commentk</router-link
      >
    </div>
    <div
      class="w-full h-screen bg-center bg-no-repeat bg-cover"
      style="
        background-image: url('https://images.unsplash.com/photo-1544747582-e90fd05971ca?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
      "
    >
      <div
        class="w-full h-screen bg-opacity-50 bg-black flex justify-center items-center"
      >
        <div class="mx-4 text-center text-white">
          <h1 class="font-bold text-6xl mb-4">Welcome to Lucky KL !</h1>
          <h2 class="font-bold text-3xl mb-8">I'm live streamer</h2>
          <h3 class="font-bold text-2xl mb-12">
            Click below to see about my gameplay
          </h3>
          <div>
            <a
              href="/gameplay"
              class="border-2 border-white rounded-md font-bold text-white px-4 py-3 transition duration-300 ease-in-out hover:bg-white hover:bg-opacity-60 hover:text-white mr-6"
            >
              Click here
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
};
</script>
