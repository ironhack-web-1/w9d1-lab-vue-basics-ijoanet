<template>
  <ul class="link-wrapper" :style="cssVars">
    <li v-for="(link, index) in links" :key="index">
      <a>{{ link }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'LinkWrapper',
  props: {
    links: {
      type: Array,
      default: () => [],
      required: true,
    },
    width: {
      type: String,
      default: '40%',
    },
    minWidth: {
      type: String,
      default: '240px',
    },
    shouldWrap: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    cssVars() {
      return {
        '--width': this.width,
        '--min-width': this.minWidth,
        '--flex-wrap': this.shouldWrap ? 'wrap' : 'nowrap',
      };
    },
  },
};
</script>

<style scoped>
.link-wrapper {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-wrap: var(--flex-wrap);

    width: var(--width);
    min-width: var(--min-width);
}
.link-wrapper > li {
    list-style: none;
}
a {
    margin: 10px;
}
</style>
