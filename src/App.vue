<template>
  <div id="app">
    <Header />
    <content-app></content-app>
    <footer-app></footer-app>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import ContentApp from './components/ContentApp/ContentApp.vue';
import FooterApp from "./components/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    ContentApp,
    FooterApp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
