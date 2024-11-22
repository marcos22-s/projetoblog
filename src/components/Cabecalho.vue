<script>
import Botao from './Botao.vue';

export default {
  name: "Cabecalho",
  props: {
    logotipo: String,
    usuario: String,
  },
  components: {
    Botao
  },
  methods: {
    obterRotaAtual() {
      console.log(this.$route.path);
      return this.$route.path;
    }
  }
}
</script>

<template>
  <header>
    <div id="cabecalho">
      <!-- Logotipo Rio 2016 -->
      <img class="logotipo" src="@/assets/rio.webp" alt="Logotipo das Olimpíadas Rio 2016">
      
      <nav class="cabecalho-col2" v-if="obterRotaAtual() != '/'">
        <Botao textoDoBotao="Login/Logout" link="/"/>
        <Botao textoDoBotao="Postagens" link="/areapostagem"/>
        <p v-if="usuario" class="usuario">Bem-vindo, {{usuario}}</p>
      </nav>
    </div>
  </header>
</template>

<style scoped>
  .logotipo {
    height: 70px;  
    padding: 10px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    max-width: 100%;  
  }

  h1 {
    font-size: 70px;
  }

  h1, h2 {
    font-weight: bolder;
  }

  .cabecalho-col2 {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
  }

  /* Estilo atualizado para o nome do usuário */
  .usuario {
    font-size: 20px;
    font-weight: bold;
    color: #ffffff; /* Cor branca */
    font-family: 'Arial', sans-serif; /* Fonte moderna */
    text-transform: uppercase; /* Para dar um toque de destaque */
    letter-spacing: 1px; /* Espaçamento entre as letras para mais destaque */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* Efeito de sombra sutil */
  }

  .cabecalho-col2 p {
    font-size: 18px;
    font-weight: bold;
    color: #333;
  }
</style>
