<script setup>
import bola from "../assets/bola.png"
</script>

<template>
    <section class="bola-natal">
        <img :src="bola" alt="">

        <div>
            <h2>Conectando generosidade
                ao redor do mundos</h2>

            <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes
                significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro
                espírito da generosidade.</p>

                <button>Fazer uma doação</button>
        </div>
    </section>
</template>

<style scoped lang="scss">
@mixin font-style($font: "Archivo", $weight: 600, $size: 40px, $lineHeight: 48px, $color: #121214) {
    font-family: $font;
    font-weight: $weight;
    font-size: $size;
    line-height: $lineHeight;
    color: $color;
}

.bola-natal{
    padding: 80px 0;
    display: flex;
    gap: 206px;

    h2{
        margin-bottom: 24px;
        @include font-style()
    }

    p{
        margin-bottom: 40px;
        @include font-style($weight: 400, $size: 24px, $lineHeight: 36px) 
    }

    button{
        width: 238px;
        padding: 14px 32px;

        border: none;
        border-radius: 4px;
        background-color: #CD3C32;

        @include font-style($font: "Roboto", $weight: 700, $size: 18px, $lineHeight: 21.09px);

        color: #FFFFFF;
    }
}

</style>