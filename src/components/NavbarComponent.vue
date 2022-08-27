<template>
  <nav>
    <img class="logo" src="../assets/logo.png" alt="Vue logo">
    <LinkContainer :links="linkList" :width="width" :min-width="minWidth" />
  </nav>
</template>

<script>
import LinkContainer from './LinkContainer.vue';

export default {
  name: 'NavbarComponent',
  components: {
    LinkContainer,
  },
  data() {
    return {
      linkList: ['Project', 'Docs', 'About us'],
      width: '30%',
      minWidth: '240px',
    };
  },
};
</script>

<style scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

a:hover {
    font-size: 18px;
    font-weight: 800;
    transition: 1s;
}

.logo {
    width: 60px;
}
</style>
