<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/liked">Liked</router-link> |
      <router-link to="/disliked">Disliked</router-link>

    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  color: #eeeeee;

}

#nav a {
  font-weight: bold;
  color: #eeeeee;
}

#nav a.router-link-exact-active {
  color: #00adb5;
}
</style>
