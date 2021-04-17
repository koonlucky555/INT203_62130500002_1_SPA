<template>
  <single-comment
    v-for="comment in comments"
    :key="comment.id"
    :comment="comment"
  />
</template>

<script>
import axios from "axios";
import SingleComment from "../components/SingleComment.vue";
export default {
  components: {
    SingleComment,
  },
  data() {
    return {
      comments: [],
      newComment: {
          name: "",
          email: "",
          message: ""
      }
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