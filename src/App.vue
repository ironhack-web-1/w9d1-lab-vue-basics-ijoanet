<template>
  <div class="app-container">
    <Navbar />
    <Math />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/NavbarComponent.vue';
import Footer from './components/FooterComponent.vue';

import Math from './components/MathComponent.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    Math,
  },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
a {
    text-decoration: none;
    cursor: pointer;
     color: #2c3e50;
    font-weight: 500;
}
</style>
