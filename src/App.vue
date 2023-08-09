<template>
  <div>
    <nav-bar />
    <header-banner />
    <main-body />
    <Footer />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import HeaderBanner from './components/HeaderBanner.vue';
import MainBody from './components/MainBody.vue';
import Footer from './components/FooterComponent.vue';

export default {
  name: 'App',
  data() {
    return {
      isUserScrolling: false,
    }
  },
  components: {
    NavBar,
    HeaderBanner,
    MainBody,
    Footer
  },
}
</script>

<style lang="scss">
@import "./assets/style/scss//general.scss";

#app {
  font-family: Urbanist, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
