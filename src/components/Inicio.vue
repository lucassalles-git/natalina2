<script setup>
//insira as lógicas
import palhaco from "../assets/logo.png";
import loja from "../assets/loja.png"
</script>

<template>
    <!-- insira as tags -->
    <section class="top">
        <div class="feliz-natal">
            <img :src="palhaco" alt="">

            <h1>Uma <span>plataforma de doação</span> para espalhar alegria</h1>

            <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>

            <button>Fazer uma doação</button>
        </div>

        <img :src="loja" alt="">
    </section>
</template>

<style scoped lang="scss">
/* insira os estilos */

/*variaveis de cores */
$main-color: #CD3C32;
$background-color1: #FFE9E8;
$background-color2: #FFD5D3;
$background-color3: #F9F9F9;

/* mixin para o estilo das fontes */
@mixin font-style($font: "Archivo", $weight: 600, $size: 40px, $lineHeight: 48px, $color: #121214) {
    font-family: $font;
    font-weight: $weight;
    font-size: $size;
    line-height: $lineHeight;
    color: $color;
}

/* section do topo */
.top {
    height: 560px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 126px;

    background-color: $background-color1;

    .feliz-natal {
        height: 351px;
        width: 590px;
        display: flex;
        flex-direction: column;
        align-items: baseline;
        justify-content: space-between;

    }

    h1 {
        @include font-style()
    }

    span {
        color: $main-color;
    }

    p {
        @include font-style($weight: 400, $size: 24px, $lineHeight: 36px);
    }

    button {
        width: 238px;
        padding: 14px 32px;

        border: none;
        border-radius: 4px;
        background-color: $main-color;

        @include font-style($font: "Roboto", $weight: 700, $size: 18px, $lineHeight: 21.09px);

        color: #FFFFFF;
    }
}
</style>