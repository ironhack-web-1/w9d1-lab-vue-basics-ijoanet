<template>
  <footer>
    <div class="info">
      <div class="name">
        Vue enjoyers
      </div>
      <div class="street">
        Fake street, 123
      </div>
      <div class="city">
        Even faker city 00000
      </div>
    </div>
    <LinkContainer :links="linkList" :should-wrap="true" />
  </footer>
</template>

<script>
import LinkContainer from './LinkContainer.vue';

export default {
  name: 'FooterComponent',
  components: {
    LinkContainer,
  },
  data() {
    return {
      linkList: ['Projects', 'Legal', 'Locations', 'Experiences', 'About us'],
      shouldWrap: true,
    };
  },
};
</script>

<style scoped>
footer {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;

    margin-top: 60px;
}
div {
    margin-bottom: 10px;
}

info > div:nth-child(2), info > div:nth-child(3) {
    margin-left: 10px;
}

.info {
    text-align: left;
}

.name {
    color: #35b05d;
    font-size: 20px;
    font-weight: 600;
}
</style>
