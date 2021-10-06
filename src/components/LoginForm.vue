<template>
  <form @submit.prevent="handleSubmit">
    <h1>
      {{ state.email }}
    </h1>
    <label for="email">email</label>
    <input
      v-model="state.email"
      type="email"
      name="email"
      id="email"
      :placeholder="emailPlaceholder"
    />
    <br />
    <label for="password">password</label>
    <input v-model="state.password" type="password" name="pass" id="pass" />
    <br>
    <button type="submit">Login</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      state: {
        email: this.emailPlaceholder,
        password: "",
      },
    };
  },
  props: {
    emailPlaceholder: String,
  },
  methods: {
    handleSubmit(event) {
      this.state.email = "";
      this.state.password = "";
    },
  },
};
</script>

<style scoped></style>
