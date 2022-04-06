<template>
  <h1>Login</h1>
  <form @submit.prevent="submit">
    <login-input v-model="mail" label="Correo" />
    <login-input v-model="psw" label="Clave" />

    <button>Log in</button>
  </form>
</template>

<script>
import LoginInput from "./LoginInput.vue";

export default {
  name: "LoginForm",
  data: () => ({ mail: "edu@edu.com", psw: "ppp" }),
  methods: {
    submit() {
      console.log(`submit ${this.mail} ${this.psw} `);
    },
  },
  components: { LoginInput },
};
</script>


