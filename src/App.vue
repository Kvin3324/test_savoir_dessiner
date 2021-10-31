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
  font-family: var(--unnamed-font-family-jost-);
  font-style: var(--unnamed-font-style-normal);
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  overflow-x: hidden;
}
</style>
