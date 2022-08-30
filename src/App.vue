<template>
  <div class="app-container">
    <Navbar /> <!-- Iteration 1 -->
    <Math /> <!-- Iteration 2 -->
    <Show :msg="showMsg" :show="true" /> <!-- Iteration 3 -->
    <Show :msg="hideMsg" :show="false" /> <!-- Iteration 3 -->
    <List /> <!-- Iteration 4 -->
    <Background /> <!-- Iteration 5 -->
    <Form /> <!-- Bonus -->
    <Footer /> <!-- Iteration 1 -->
  </div>
</template>

<script>
import Navbar from './components/NavbarComponent.vue';
import Footer from './components/FooterComponent.vue';

import Math from './components/MathComponent.vue';

import Show from './components/ShowComponent.vue';

import List from './components/ListComponent.vue';

import Background from './components/BackgroundComponent.vue';

import Form from './components/FormComponent.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
    Math,
    Show,
    List,
    Background,
    Form,
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
