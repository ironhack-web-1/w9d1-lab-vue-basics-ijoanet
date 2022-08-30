<template>
  <div class="math-wrapper">
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
.math-wrapper {
    margin: 100px;
}
</style>
