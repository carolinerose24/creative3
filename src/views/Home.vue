<template>
  <div class="first">
    <h1>Conspiracies</h1>
    <ArticleList :articles="articles"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ArticleList from "../components/ArticleList.vue";

export default {
  name: "Home",
  components: {
    ArticleList
  },
  data() {
    return {
    }
  },
  computed: {
    articles() {
      return this.$root.$data.articles;
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
