<template>
  <nav class="select-none bg-white lg:flex lg:items-stretch w-full fixed" id="nav">
    <div class="flex flex-no-shrink items-stretch h-16">
      <router-link to="/" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center 
      hover:bg-gray-800  hover:text-white "
        >Home</router-link
      >
    </div>
    <div class="lg:flex lg:items-stretch lg:flex-no-shrink lg:flex-grow">
      <div class="lg:flex lg:items-stretch lg:justify-end ml-auto">
        <router-link to="/about" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center
          hover:bg-gray-800  hover:text-white"
          >About Me</router-link
        >
        <router-link to="/gameplay" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center 
         hover:bg-gray-800   hover:text-white"
          >GamePlay</router-link
        >
        <router-link to="/comment" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center 
         hover:bg-gray-800   hover:text-white"
          >Comment</router-link
        >
      </div>
    </div>
  </nav>
</template>

<style scoped>
#nav a.router-link-exact-active {
  color: #42b983;
}
</style>