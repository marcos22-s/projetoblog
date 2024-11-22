<script>
    export default {
        props: {
            titulo: String,
            corpoDoTexto: String,
            autor: String,
            imagem: String
        }
    }
</script>

<template>
    <div class="post">
        <!-- Imagem do Post -->
        <img :src="imagem" class="imagem-post" alt="Imagem do post" />
        <!-- Título da Postagem -->
        <h2>{{titulo}}</h2>
        <!-- Corpo do Texto -->
        <p>{{corpoDoTexto}}</p>
        <!-- Autor do Post -->
        <p class="autor">por {{autor}}</p>
    </div>
</template>

<style scoped>
    /* Centralizando a imagem do post e com borda dourada */
    .imagem-post {
        width: 100%;
        max-width: 600px;
        height: auto;
        border-radius: 12px; /* Bordas arredondadas */
        border: 5px solid #ffcd00; /* Borda dourada (referência às medalhas olímpicas) */
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* Sombra suave para a imagem */
        margin-bottom: 20px; /* Espaçamento abaixo da imagem */
    }

    /* Estilo do título da postagem com fontes e cores inspiradas nas Olimpíadas */
    h2 {
        font-size: 2.2em;
        color: #004b87; /* Azul olímpico */
        font-weight: bold;
        margin-top: 20px;
        margin-bottom: 15px;
        text-transform: uppercase;
        letter-spacing: 2px; /* Espaçamento para mais destaque */
        text-align: center; /* Centraliza o título */
    }

    /* Corpo do texto da postagem com foco na legibilidade */
    p {
        font-size: 1.1em;
        line-height: 1.6;
        color: #333; /* Cor de texto neutra para boa leitura */
        margin-bottom: 20px;
    }

    /* Estilo do autor, utilizando o azul olímpico */
    .autor {
        font-size: 1em;
        font-weight: bold;
        color: #004b87; /* Azul olímpico */
        text-align: center;
        margin-top: 10px;
    }

    /* Estilos principais do Post */
    .post {
        background-color: #fff;
        border-radius: 12px;
        padding: 20px;
        margin-bottom: 30px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        border-left: 6px solid #ffcd00; /* Borda dourada à esquerda, representando o ouro */
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    /* Efeito de hover para o post, aumentando a interação */
    .post:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 15px rgba(0, 0, 0, 0.15);
    }

    /* Adicionando um toque olímpico de destaque no post */
    .post:hover {
        border-left: 6px solid #ff4f00; /* Quando hover, a borda dourada muda para laranja olímpico */
    }
</style>
