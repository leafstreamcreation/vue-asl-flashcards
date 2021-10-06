<template>
  <div>
    <h1>{{ toggleSignup }}</h1>
    <div class="main">
      <input v-model="toggleSignup" type="checkbox" name="toggle" id="toggle" />
      <login-form v-if="!toggleSignup" emailPlaceholder="example@gmail.com" />
      <signup-form emailPlaceholder="example@gmail.com" v-else />
    </div>
  </div>
</template>

<script>
import LoginForm from "../components/LoginForm.vue";
import SignupForm from "../components/SignupForm.vue";

export default {
  data() {
    return {
      toggleSignup: false,
    };
  },
  components: {
    "login-form": LoginForm,
    "signup-form": SignupForm,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  margin: 0;
  padding: 0;
}

.main {
  width: 100vw;
  background-color: #42b983;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
