<template>
<div class="wrapper">
  <div class="articles">
    <div class="article" v-for="article in articles" :key="article.id">



    <div class="individual-article">


    <div class="image">
      <img :src="'/images/articles/'+article.image">
    </div>
      <div class="info">
        <h1>{{article.title}}</h1>
        <h2>{{article.subtitle}}</h2>
        <p>{{article.creator}}, {{article.date}}</p>

      </div>

      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'LikedList',
  props: {
    liked: Array
  },
  methods: {
    like(article){
      this.$root.$data.liked.push(article);
    },
    dislike(article){
      this.$root.$data.disliked.push(article);
    }
  }
}
</script>








<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}


.articles {

}


.individual-article {
  display: flex;
  margin: 48px 0;
  background-color: #18b0b0;

}


 img {
  height: 250px;

  //object-fit: fill;

  border-top: 8px solid #18b0b0;
  margin-left: 8px;

}


.info {
  background: #18b0b0;
  color: #000;
  padding: 10px 30px;
  height: 80px;
}

.info h1 {
  font-size: 24px;
}

.info h2 {
  font-size: 20px;
}

.info p {
  margin: 0px;
  font-size: 14px;
}


.buttons {
  display: flex;
  margin: 16px 0 0 0;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
  padding: 0 14px;

  margin: 0 4px;
}

.auto {
  margin-left: auto;
}
</style>
