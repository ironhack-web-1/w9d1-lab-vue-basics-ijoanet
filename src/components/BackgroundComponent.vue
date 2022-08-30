<template>
  <div :style="bgStyle" class="background-wrapper" @click="backgroundToggle = !backgroundToggle">
    <div>Click me!</div>
  </div>
</template>

<script>
export default {
  name: 'BackgroundComponent',
  data() {
    return {
      backgroundToggle: false,
    };
  },
  computed: {
    bgStyle() {
      if (this.backgroundToggle) {
        return {
          background: 'black',
          color: 'white',
        };
      }
      return {
        background: 'lightgray',
        color: 'black',
      };
    },
  },
};
</script>

<style scoped>
.background-wrapper {
    width: 100%;
    height: 300px;

    display: flex;
    align-items: center;
    justify-content: center;

    margin: 100px 0;

    font-size: 30px;
    font-weight: 600;
}
</style>
