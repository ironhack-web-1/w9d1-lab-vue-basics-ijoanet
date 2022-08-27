<template>
  <div class="math-container">
    2 + 2 = {{ sum(2, 2) }}
  </div>
</template>

<script>

export default {
  name: 'MathComponent',
  methods: {
    sum(a, b) {
      return `${a + b}`;
    },
  },
};
</script>

<style scoped>
.math-container {
    margin: 300px;
}
</style>
