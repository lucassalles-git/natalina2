<script setup>
//insira as lógicas
import palhaco from "../assets/logo.png";
import loja from "../assets/loja.png"
</script>

<template>
    <!-- insira as tags -->
    <section class="top">
        <div class="feliz-natal">
            <img class="logo" :src="palhaco" alt="">

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

    @media (max-width: 440px) and (max-height: 956px) {
        height: auto;
        padding: 96px 24px;
        flex-direction: column;
        gap: 64px;
        text-align: center;
    }

    .feliz-natal {
        height: 351px;
        width: 570px;
        display: flex;
        flex-direction: column;
        align-items: baseline;
        justify-content: space-between;

        @media (max-width: 440px) and (max-height: 956px) {
            width: 100%;
            align-items: center;
            justify-content: center;
            gap: 30px;
        }

        .logo {
            @media (max-width: 440px) and (max-height: 956px) {
                width: 160px;
                height: 38px;
            }
        }

    }

    h1 {
        @include font-style();

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 32px, $lineHeight: 38.4px);

            width: 240px;
        }
    }

    span {
        color: $main-color;
    }

    p {
        @include font-style($weight: 400, $size: 24px, $lineHeight: 36px);

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 18px, $lineHeight: 27px);

            width: 86vw;
        }
    }

    button {
        width: 238px;
        padding: 14px 32px;

        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.226);
        border: none;
        border-radius: 4px;
        background-color: $main-color;
        transition: all 0.5s;

        @include font-style($font: "Roboto", $weight: 700, $size: 18px, $lineHeight: 21.09px, $color: #FFFFFF);

        @media (max-width: 440px) and (max-height: 956px) {
            width: 100%;
            padding: 16px 32px;
        }

    }

    button:hover {
        transition: all 0.5s;
        background-color: #2B5E57;
    }

    img {
        @media (max-width: 440px) and (max-height: 956px) {
            width: 326px;
            height: 221.03px;
        }
    }
}
</style>