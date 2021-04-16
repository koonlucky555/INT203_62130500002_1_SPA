<template>
  <div class="about w-full grid grid-cols-3">
    <div id="nav" class="absolute w-full p-12">
      <router-link to="/" class="text-black hover:text-gray-500 text-xl"
        >Home</router-link
      >
      |
      <router-link to="/about" class="text-black hover:text-gray-500 text-xl"
        >About</router-link
      >
    </div>

    <div
      class="w3-container w3-content w3-center w3-padding-64 col-start-2 grid grid-flow-row auto-rows-max"
      style="max-width: 800px"
      id="band"
    >
      <img :src="img" alt="lucky" class="rounded-full h-80 w-80 justify-self-center">
      <h2 class="w3-wide pt-4">Lucky KL</h2>
      <p class="w3-opacity justify-self-center"><i>I love music</i></p>
      <p class="w3-justify justify-self-center">{{name}}</p> 
      <p class="w3-justify justify-self-center">{{birth}}</p>
      <p class="w3-justify justify-self-center">{{faculty}}</p>
     
      <div class="pl-20 flex justify-self-center pt-8">
       
       <a href="https://www.facebook.com/profile.php?id=100010625265031" >
        <svg height="40%" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;" version="1.1" viewBox="0 0 512 512" 
        width="40%"  xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:serif="http://www.serif.com/" xmlns:xlink="http://www.w3.org/1999/xlink"><g><path d="M512,256c0,-141.385 -114.615,-256 -256,-256c-141.385,0 -256,114.615 -256,256c0,127.777 93.616,233.685 216,252.89l0,-178.89l-65,0l0,-74l65,0l0,-56.4c0,-64.16 38.219,-99.6 96.695,-99.6c28.009,0 57.305,5 57.305,5l0,63l-32.281,0c-31.801,0 -41.719,19.733 -41.719,39.978l0,48.022l71,0l-11.35,74l-59.65,0l0,178.89c122.385,-19.205 216,-125.113 216,-252.89Z" style="fill:#1877f2;fill-rule:nonzero;"/><path d="M355.65,330l11.35,-74l-71,0l0,-48.022c0,-20.245 9.917,-39.978 41.719,-39.978l32.281,0l0,-63c0,0 -29.297,-5 -57.305,-5c-58.476,0 -96.695,35.44 -96.695,99.6l0,56.4l-65,0l0,74l65,0l0,178.89c13.033,2.045 26.392,3.11 40,3.11c13.608,0 26.966,-1.065 40,-3.11l0,-178.89l59.65,0Z" style="fill:#fff;fill-rule:nonzero;"/></g></svg>
       </a>
      
        <a href="https://www.twitch.tv/koonlucky" >
          <svg height="40%" width="40%"   enable-background="new 0 0 50 50" id="Layer_1" version="1.1" viewBox="0 0 50 50" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path d="M45,1H5C2.8,1,1,2.8,1,5v40c0,2.2,1.8,4,4,4h40c2.2,0,4-1.8,4-4V5C49,2.8,47.2,1,45,1z" fill="#6441A5"/><g id="_x7C___x7C_"><path d="M31,36h-6l-3,4h-4v-4h-7V15.1l2-5.1h26v18L31,36z M36,27V13H15v19h6v4l4-4h6L36,27z" fill="#FFFFFF" id="Dialog"/><rect fill="#FFFFFF" height="8" id="_x7C_" width="3" x="28" y="18"/><rect fill="#FFFFFF" height="8" id="_x7C__2_" width="3" x="22" y="18"/></g></svg>
        </a>
         
        <a href="https://www.instagram.com/luckyyy_kl/">
          <svg height="40%" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;" version="1.1" viewBox="0 0 512 512" 
          width="40%"  xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:serif="http://www.serif.com/" xmlns:xlink="http://www.w3.org/1999/xlink"><g><path d="M256,0c-69.526,0 -78.244,0.295 -105.549,1.541c-27.248,1.243 -45.858,5.57 -62.142,11.899c-16.834,6.542 -31.111,15.296 -45.342,29.528c-14.232,14.231 -22.986,28.508 -29.528,45.342c-6.329,16.283 -10.656,34.893 -11.899,62.141c-1.246,27.305 -1.54,36.023 -1.54,105.549c0,69.524 0.294,78.242 1.54,105.547c1.243,27.248 5.57,45.858 11.899,62.141c6.542,16.834 15.296,31.111 29.528,45.344c14.231,14.231 28.508,22.985 45.342,29.527c16.284,6.328 34.894,10.656 62.142,11.899c27.305,1.245 36.023,1.54 105.549,1.54c69.524,0 78.242,-0.295 105.547,-1.54c27.248,-1.243 45.858,-5.571 62.141,-11.899c16.834,-6.542 31.111,-15.296 45.344,-29.527c14.231,-14.233 22.985,-28.51 29.527,-45.344c6.328,-16.283 10.656,-34.893 11.899,-62.141c1.245,-27.305 1.54,-36.023 1.54,-105.547c0,-69.526 -0.295,-78.244 -1.54,-105.549c-1.243,-27.248 -5.571,-45.858 -11.899,-62.141c-6.542,-16.834 -15.296,-31.111 -29.527,-45.342c-14.233,-14.232 -28.51,-22.986 -45.344,-29.528c-16.283,-6.329 -34.893,-10.656 -62.141,-11.899c-27.305,-1.246 -36.023,-1.541 -105.547,-1.541Zm0,46.127c68.354,0 76.451,0.26 103.445,1.492c24.959,1.139 38.514,5.309 47.535,8.814c11.949,4.644 20.477,10.192 29.435,19.15c8.959,8.958 14.506,17.487 19.15,29.435c3.506,9.021 7.676,22.576 8.815,47.535c1.231,26.995 1.492,35.092 1.492,103.447c0,68.354 -0.261,76.451 -1.492,103.445c-1.139,24.959 -5.309,38.514 -8.815,47.535c-4.644,11.949 -10.191,20.477 -19.15,29.435c-8.958,8.959 -17.486,14.506 -29.435,19.15c-9.021,3.506 -22.576,7.676 -47.535,8.814c-26.99,1.232 -35.086,1.493 -103.445,1.493c-68.361,0 -76.455,-0.261 -103.447,-1.493c-24.959,-1.138 -38.514,-5.308 -47.535,-8.814c-11.949,-4.644 -20.477,-10.191 -29.436,-19.15c-8.958,-8.958 -14.506,-17.486 -19.149,-29.435c-3.506,-9.021 -7.676,-22.576 -8.815,-47.535c-1.232,-26.994 -1.492,-35.091 -1.492,-103.445c0,-68.355 0.26,-76.452 1.492,-103.447c1.139,-24.959 5.309,-38.514 8.815,-47.535c4.643,-11.948 10.191,-20.477 19.149,-29.435c8.959,-8.958 17.487,-14.506 29.436,-19.15c9.021,-3.505 22.576,-7.675 47.535,-8.814c26.995,-1.232 35.092,-1.492 103.447,-1.492Z" style="fill:url(#_Linear1);fill-rule:nonzero;"/><path d="M256,341.332c-47.129,0 -85.334,-38.205 -85.334,-85.332c0,-47.129 38.205,-85.334 85.334,-85.334c47.127,0 85.332,38.205 85.332,85.334c0,47.127 -38.205,85.332 -85.332,85.332Zm0,-216.792c-72.604,0 -131.46,58.856 -131.46,131.46c0,72.602 58.856,131.458 131.46,131.458c72.602,0 131.458,-58.856 131.458,-131.458c0,-72.604 -58.856,-131.46 -131.458,-131.46Z" style="fill:url(#_Linear2);fill-rule:nonzero;"/><path d="M423.372,119.346c0,16.967 -13.754,30.72 -30.72,30.72c-16.966,0 -30.72,-13.753 -30.72,-30.72c0,-16.966 13.754,-30.719 30.72,-30.719c16.966,0 30.72,13.753 30.72,30.719Z" style="fill:url(#_Linear3);fill-rule:nonzero;"/></g><defs><linearGradient gradientTransform="matrix(-149.618,494.3,-494.3,-149.618,300.81,-27.1283)" gradientUnits="userSpaceOnUse" id="_Linear1" x1="0" x2="1" y1="0" y2="0"><stop offset="0" style="stop-color:#515bd4;stop-opacity:1"/><stop offset="0.26" style="stop-color:#9510b8;stop-opacity:1"/><stop offset="0.66" style="stop-color:#e51804;stop-opacity:1"/><stop offset="1" style="stop-color:#feda77;stop-opacity:1"/></linearGradient><linearGradient gradientTransform="matrix(-149.618,494.3,-494.3,-149.618,300.81,-27.1283)" gradientUnits="userSpaceOnUse" id="_Linear2" x1="0" x2="1" y1="0" y2="0"><stop offset="0" style="stop-color:#515bd4;stop-opacity:1"/><stop offset="0.26" style="stop-color:#9510b8;stop-opacity:1"/><stop offset="0.66" style="stop-color:#e51804;stop-opacity:1"/><stop offset="1" style="stop-color:#ffbf00;stop-opacity:1"/></linearGradient><linearGradient gradientTransform="matrix(-149.618,494.3,-494.3,-149.618,300.81,-27.1283)" gradientUnits="userSpaceOnUse" id="_Linear3" x1="0" x2="1" y1="0" y2="0"><stop offset="0" style="stop-color:#515bd4;stop-opacity:1"/><stop offset="0.26" style="stop-color:#9510b8;stop-opacity:1"/><stop offset="0.66" style="stop-color:#e51804;stop-opacity:1"/><stop offset="1" style="stop-color:#ffbf00;stop-opacity:1"/></linearGradient></defs></svg>
        </a>
         
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      nickname:"Lucky KL",
      name:"Kanokporn Buaycharoen",
      birth:"29 September 2000",
      img: require("../assets/lucky.jpg"),
      faculty:"School of Information Technology"
    }
  }
}
</script>