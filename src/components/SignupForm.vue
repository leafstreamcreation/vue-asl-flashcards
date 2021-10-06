<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{this.state.email}}</h1>
    <label for="email">email</label>
    <input v-model="state.email" type="email" name="email" id="email" :placeholder="emailPlaceholder">
    <br>
    <label for="password">password</label>
    <input v-model="state.password" type="password" name="password" id="password">
    <br>
    <label for="passwordValidate">re-enter password</label>
    <input v-model="state.passwordValidate" type="password" name="passwordValidate" id="passwordValidate">
    <br>
    <button type="submit">Sign Up</button>
  </form>
</template>

<script>
export default {
  props: {
    emailPlaceholder: String,
  },
  data() {
    return {
      state: {
        email: this.emailPlaceholder,
        password: '',
        passwordValidate: ''
      }
    }
  },
  methods: {
    handleSubmit() {
      this.state.email = '';
      this.state.password = '';
      this.state.passwordValidate = '';
    }
  }
};
</script>

<style scoped></style>
