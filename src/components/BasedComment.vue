<template>
     <div v-for="comment in comments" :key="comment.id">
      <div class="bg-black pt-32 grid grid-cols-3 p-32 justify-items-center">
        <div class="mb-20 mr-20 rounded overflow-hidden shadow-lg">
          <div class="bg-white px-32 py-16">
            <p class="text-black text-lg"><b>{{comment.name}}</b></p>
            <p class="text-black text-xl"><b>{{comment.email}}</b></p>
            <p class="text-black text-md"><b>{{comment.message}}</b></p>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      comments: [],
    };
  },
  mounted() {
    axios.get("http://localhost:5000/formdata").then((res) => {
      this.comments = res.data;
      console.log(this.comments);
    });
  },
};
</script>