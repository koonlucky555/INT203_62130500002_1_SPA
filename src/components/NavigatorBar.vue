<template>
  <nav class="relative select-none bg-white lg:flex lg:items-stretch w-full">
    <div class="flex flex-no-shrink items-stretch h-16">
      <router-link to="/" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center hover:bg-grey-dark"
        >Home</router-link
      >
    </div>
    <div class="lg:flex lg:items-stretch lg:flex-no-shrink lg:flex-grow">
      <div class="lg:flex lg:items-stretch lg:justify-end ml-auto">
        <router-link to="/about" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center hover:bg-grey-dark"
          >About Me</router-link
        >
        <router-link to="/gameplay" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center hover:bg-grey-dark"
          >GamePlay</router-link
        >
        <router-link to="/comment" class="flex-no-grow flex-no-shrink relative py-3 px-6 leading-normal text-black no-underline flex items-center hover:bg-grey-dark"
          >Comment</router-link
        >
      </div>
    </div>
  </nav>
</template>