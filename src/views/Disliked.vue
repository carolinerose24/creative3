<template>
  <div class="first">
    <h1>Conspiracies I don't believe (yet)</h1>
    <h1 v-if="this.$root.$data.disliked.length == 0">(empty...for now)</h1>
    <ArticleList :articles="articles"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ArticleList from "../components/ArticleList.vue";

export default {
  name: "Disliked",
  components: {
    ArticleList
  },
  data() {
    return {
    }
  },
  computed: {
    articles() {
      return this.$root.$data.disliked;
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
