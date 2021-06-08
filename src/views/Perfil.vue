<template>
  <div>
    <a :href="link">Google</a>

    <div :style="{ color: cor, background: fundo }">OI</div>

    <div class="lista">
      <li v-for="item in itens" :key="item">
        <span>O item {{ item.nome }} custa: {{ item.valor }}</span>
      </li>
    </div>

    <label for="email">Email</label><br />
    <input v-model.trim.lazy="email" type="email" /><br />
    <label for="senha">Senha</label><br />
    <input v-model.lazy="senha" type="password" /><br />
    <label for="idade">Idade</label><br />
    <input v-model.number.lazy="idade" type="number" /><br />

    <span>Email: {{ email }}</span
    ><br />
    <span>Senha: {{ senha }}</span
    ><br />
    <span>Idade: {{ idade }}</span>
  </div>
</template>

<script>
export default {
  data: () => ({
    link: "http://google.com.br",

    cor: "red",
    fundo: "black",

    itens: [
      { nome: "Copo", valor: "R$5,00" },
      { nome: "Faca", valor: "R$10,00" },
      { nome: "Prato", valor: "R$15,00" },
    ],

    email: "",
    senha: "",
    idade: "",
  }),
};
</script>

<style></style>
