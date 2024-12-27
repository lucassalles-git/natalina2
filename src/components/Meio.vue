<script setup>
import presentes from "../assets/presentes.png"
import Fim from "./Fim.vue";
import Contador from "./Contador.vue";
</script>

<template>
    <main>
        <section class="tempo-limitado">
            <div>
                <h2>Tempo limitado</h2>

                <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.
                </p>
            </div>

            <p class="contador"><Contador/></p>

            <img class="presente" :src="presentes" alt="">
        </section>
        <Fim />
    </main>
</template>

<style scoped lang="scss">
@mixin font-style($font: "Archivo", $weight: 600, $size: 40px, $lineHeight: 48px, $color: #121214) {
    font-family: $font;
    font-weight: $weight;
    font-size: $size;
    line-height: $lineHeight;
    color: $color;
}

main {
    padding: 0 352px;

    @media (max-width: 440px) and (max-height: 956px) {
        padding: 8px 0;
    }

    @media (max-width: 884px) and (max-height: 1280px) {
        padding: 0;
    }

}

.tempo-limitado {
    padding: 80px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;

    @media (max-width: 440px) and (max-height: 956px) {
        padding: 80px 24px;
        align-items: center;
        gap: 24px;
    }

    div {
        width: 477px;

        @media (max-width: 440px) and (max-height: 956px) {
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    }

    h2 {
        margin-bottom: 24px;
        @include font-style($lineHeight: 43.52px);
        text-align: center;

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 32px, $lineHeight: 34.82px);
        }
    }

    p {
        @include font-style($weight: 400, $size: 20px, $lineHeight: 30px);
        text-align: center;

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 18px, $lineHeight: 27px);
            width: 87vw;
        }
    }

    .contador {
        @include font-style($size: 64px, $lineHeight: 69.63px, $color: #CD3C32);

        @media (max-width: 440px) and (max-height: 956px) {
            @include font-style($size: 32px, $lineHeight: 34.82px, $color: #CD3C32);

            width: 95vw;
        }

        @media (max-width: 884px) and (max-height: 1280px) {
            width: 77vw;
        }

    }

    .presente {
        @media (max-width: 440px) and (max-height: 956px) {
            width: 85vw;
            height: 209.38px;
        }
    }
}
</style>