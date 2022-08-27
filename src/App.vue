<template>
  <div class="app-container">
    <Navbar />
    <Math />
    <Show :msg="showMsg" :show="true" />
    <Show :msg="hideMsg" :show="false" />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/NavbarComponent.vue';
import Footer from './components/FooterComponent.vue';

import Math from './components/MathComponent.vue';

import Show from './components/ShowComponent.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    Math,
    Show,
  },
  data() {
    return {
      showMsg: 'This message should be shown!👀',
      hideMsg: 'This message should not be shown!😢',
    };
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
