<template>
  <div class="first">
    <h1>Conspiracies I believe</h1>
    <h1 v-if="this.$root.$data.liked.length == 0">(empty...for now)</h1>
    <ArticleList :articles="articles"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ArticleList from "../components/ArticleList.vue";

export default {
  name: "Liked",
  components: {
    ArticleList
  },
  data() {
    return {
    }
  },
  computed: {
    articles() {
      return this.$root.$data.liked;
    }
  },
};
</script>


<style scoped>

body {
background-color: black;
}

h1 {
  color: #eeeeee;
  font-family: monospace;
}

</style>
