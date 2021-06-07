<template>
  <div class="login">
    <h3>LOGIN</h3>
    <label for="email">Email:</label> <br />
    <input v-model="email" type="email" /><br />

    <label for="senha">Senha:</label><br />
    <input v-model="senha" type="password" /> <br /><br />
    <button @click="login" target="_blank">ENTRAR</button>
  </div>
</template>

<script>
export default {
  data: () => ({
    email: "",
    senha: "",
  }),
  methods: {
    login() {
      if (this.email == "lara" && this.senha == "123") {
        let route = this.$router.resolve({ path: "../views/Perfil.vue" });
        window.open(route.href, "_blank");
      } else {
        console.log("erro");
      }
      console.log(this.email);
    },
  },
};
</script>

<style scoped>
.login {
  box-shadow: 1px 1px 10px 1px rgb(202, 202, 202);
}
</style>
