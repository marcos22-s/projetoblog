<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import rio from './assets/rio.webp'
import carro from './assets/carro.webp'
import volei from './assets/volei.webp'
import ouro from './assets/ouro.webp'


</script>

<template style="background-color: white;">

<img :src="rio" alt="rio"> 



<br>
<p></p>

<div class="postagem2" style="text-align: center;">
<h1 style="color: black; font-family:Georgia, 'Times New Roman', Times, serif;">Classificação da nossa seleção vem?</h1>
<img :src="volei" alt="volei"; width="800px" height="500px">
<h3 style="color: black;font-family:Georgia, 'Times New Roman', Times, serif">A judoca brasileira Beatriz Souza conquistou a primeira medalha de ouro do Brasil nas Olimpíadas de Paris ao vencer na final a israelense Raz Hershko, número 2 do ranking mundial, na categoria +78kg. Mas, afinal, quanto Beatriz Souza vai receber em dinheiro pelo ouro?
</h3>
</div>

<br>
<p></p>

<div class="postagem2" style="text-align: center;">
<h1 style="color: black;font-family:Georgia, 'Times New Roman', Times, serif">NOSSO PRIMEIRO OUROO!!!!</h1>
<img :src="ouro" alt="ouro"; width="800px" height="500px">
<h3 style="color: black;font-family:Georgia, 'Times New Roman', Times, serif">O resultado das últimas eleições presidenciais na Venezuela levaram o país a uma onda de protestos. De acordo com o Conselho Nacional Eleitoral (CNE), Nicolás Maduro, sucessor de Hugo Chávez, foi reeleito com 51,2% dos votos.

 

 <footer>
        <p>&copy; 2024 Meu Site. Todos os direitos reservados.</p>
        <p>
            <a href="/privacidade.html">Política de Privacidade</a> |
            <a href="/contato.html">Contato</a>
        </p>
    </footer>
 
</h3>
</div>




</template>

<style scoped>
header {
  line-height: 1.5;
}

template{
  background-color: white;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    height: 20px;
    width: 30px;
    position: center;
  }

  template{
    background-color: white;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
