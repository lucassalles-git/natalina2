<script setup>
import bola from "../assets/bola.png"
</script>

<template>
    <section class="bola-natal">
        <img class="ball" :src="bola" alt="Mãos segurando uma bola de natal">

        <div>
            <h2>Conectando generosidade
                ao redor do mundo</h2>

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

.bola-natal {
    padding: 80px 0;
    display: flex;
    gap: 206px;

    @media (max-width: 440px) and (max-height: 956px) {
        padding: 80px 24px;
        flex-direction: column;
        align-items: center;
        gap: 48px;

        text-align: center;
    }

    @media (min-width: 768px) and (max-width: 884px) and (max-height: 1280px) {
        padding: 80px 83px;
        width: 100vw;
        flex-direction: column;
        align-items: center;
        gap: 48px;

        text-align: center;
    }

    .ball {
        @media (max-width: 440px) and (max-height: 956px) {
            width: 213.94px;
            height: 206.6px;
        }
    }

    div {

        @media (max-width: 440px) and (max-height: 956px) {
            width: 100%;
        }

        @media (max-width: 884px) and (max-height: 1280px) {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    }

    h2 {
        margin-bottom: 24px;
        @include font-style();

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 32px, $lineHeight: 38.4px);

        }

        @media (max-width: 884px) and (max-height: 1280px) {
            width: 64vw;
        }
    }

    p {
        margin-bottom: 40px;
        @include font-style($weight: 400, $size: 24px, $lineHeight: 36px);

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 18px, $lineHeight: 27px);
        }
    }

    button {
        width: 238px;
        padding: 14px 32px;

        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.226);
        border: none;
        border-radius: 4px;
        background-color: #CD3C32;
        transition: all 0.5s;

        @include font-style($font: "Roboto", $weight: 700, $size: 18px, $lineHeight: 21.09px, $color: #FFFFFF);

        @media (max-width: 440px) and (max-height: 956px) {
            width: 100%;
            padding: 16px 32px;
        }
    }

    button:hover {
        transition: all 0.5s;
        background-color: #C4A16A;
    }
}
</style>