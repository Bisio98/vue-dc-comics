<template>
  <div id="app">
    <Header/>
    <Body/>
    <Footer/>
  </div>
</template>

<script>
import Body from "./components/Body.vue";
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Body,
    Footer
  },
}
    Body;
</script>

<style>
  @import './style/general.scss';
  
</style>
