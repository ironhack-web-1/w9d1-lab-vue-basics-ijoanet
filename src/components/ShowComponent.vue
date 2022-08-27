<template>
  <div class="show-container">
    <div v-if="show" class="shown-item">
      {{ msg }}<div />
    </div>
  </div>
</template>

<script>

export default {
  name: 'ShowComponent',
  props: {
    msg: {
      type: String,
      default: 'Placeholder',
    },
    show: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.show-container {
    margin: 100px;
}
div {
    font-weight: 700;
    font-size: 20px;
}
</style>
