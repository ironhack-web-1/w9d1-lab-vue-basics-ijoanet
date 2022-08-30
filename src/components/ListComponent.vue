<template>
  <ul class="list-wrapper">
    <li v-for="(item, index) in list" :key="index">
      <a>{{ item }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ListComponent',
  props: {
    links: {
      type: Array,
      default: () => [],
      required: true,
    },
  },
  data() {
    return {
      list: [
        'Item one',
        'Item two',
        'Item three',
      ],
    };
  },
};
</script>

<style scoped>
.list-wrapper {
    margin: 100px;
}
.list-wrapper li {
    list-style: none;
}
</style>
