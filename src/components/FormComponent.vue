<template>
  <div class="form-wrapper">
    <h1>This is a form</h1>
    <form>
      <input v-model="name" type="text" placeholder="name">
      <input v-model="email" type="email" placeholder="email">
    </form>
    <h1>This is the two-way-data-binding result:</h1>
    <div>Your name is: {{ name }}</div>
    <div>Your email is: {{ email }}</div>
  </div>
</template>

<script>
export default {
  name: 'FormComponent',
  data() {
    return {
      name: undefined,
      email: undefined,
    };
  },
};
</script>

<style scoped>
.form-wrapper {
    margin: 100px 0;
}
input {
    display: -webkit-box;
    margin: auto;
}
</style>
