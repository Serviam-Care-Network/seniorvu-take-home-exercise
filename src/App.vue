<template>
  <div id="app">
    <header>
      <img class="logo" src="./assets/seniorvu-logo.svg">
    </header>

    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
};
</script>

<style>
body {
  background-color: white;
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

h1 {
  margin: 0;
  color: gray;
  border-bottom: 1px solid lightgray;
}

header {
  margin: 20px;
  text-align: right;
}

.logo {
  height: 40px;
}

.container {
  padding: 20px 40px;
}
</style>
