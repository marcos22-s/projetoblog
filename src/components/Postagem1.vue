<script setup>
    import PostModelo from "./PostModel.vue"
    import imagemPost1 from "../assets/volei.webp"
    import imagemPost2 from "../assets/simbolo.webp"
</script>

<template>
  <div>
    <!-- Primeira Postagem -->
    <div class="post">
        <PostModelo 
          titulo="Brasil é Ouroooo"
          corpoDoTexto="
          Bia conquista Ouro nos Jogos Olímpicos!

A atleta Bia fez história nos Jogos Olímpicos ao conquistar a medalha de ouro, mostrando toda a sua habilidade, determinação e espírito olímpico. Com uma performance impecável, ela superou os desafios da competição, demonstrando sua força mental e técnica refinada.

Desde o início de sua trajetória esportiva, Bia se destacou pelo seu comprometimento e trabalho árduo, e essa vitória é a recompensa de anos de esforço. Sua conquista não é apenas um reflexo do seu talento, mas também de sua paixão pelo esporte e pela busca incessante pela perfeição.
          "
          autor="Marquinhos"
          :imagem="imagemPost1"
        />
    </div>

    <!-- Segunda Postagem -->
    <div class="post">
        <PostModelo 
          titulo="O Espírito Olímpico!"
          corpoDoTexto="
          O símbolo das Olimpíadas representa muito mais do que uma competição esportiva. Ele é um emblema da união entre diferentes culturas, países e atletas de todas as partes do mundo. Os cinco anéis entrelaçados simbolizam a fraternidade global e a busca pela excelência.

Ao longo da história, as Olimpíadas têm sido palco de momentos de superação, emoção e orgulho. Cada competição, cada atleta, traz consigo uma história única, marcada por dedicação, sacrifícios e, acima de tudo, o amor pelo esporte.

Com o símbolo das Olimpíadas, comemoramos não apenas a vitória individual, mas a união global em torno de um ideal comum: a busca pela paz e pela solidariedade, em meio à competição saudável e ao respeito mútuo.
          "
          autor="Marquinhos"
          :imagem="imagemPost2"
        />
    </div>
  </div>
</template>

<style scoped>
    /* Estilo para a imagem do post */
    img {
        width: 100%;
        max-width: 600px;
        border-radius: 10px;
        border: 4px solid #ffcd00;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .autor {
        font-size: 1em;
        font-weight: bold;
        color: #004b87;
        margin-top: 10px;
    }

    /* Estilos comuns para ambas as postagens */
    .post {
        background-color: #fff;
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 20px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        border-left: 6px solid #ffcd00;
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .post:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 15px rgba(0, 0, 0, 0.15);
    }

    /* Título da postagem */
    .post h2 {
        font-size: 2em;
        color: #004b87;
        font-weight: bold;
        margin-bottom: 10px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .post p {
        font-size: 1.1em;
        line-height: 1.6;
        color: #333;
        margin-bottom: 20px;
    }

    .post {
        border-left: 6px solid #ffcd00;
    }
</style>
