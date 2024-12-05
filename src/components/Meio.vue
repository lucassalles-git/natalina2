<script setup>
import presentes from "../assets/presentes.png"
import Fim from "./Fim.vue";
</script>

<template>
    <main>
        <section class="tempo-limitado">
            <div>
                <h2>Tempo limitado</h2>

                <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.
                </p>
            </div>

            <p class="contador">10d -24h - 01m  - 52s</p>

            <img :src="presentes" alt="">
        </section>
        <Fim/>
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
}

.tempo-limitado {
    padding: 80px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;

    div{
        width: 477px;
    }

    .contador{
        @include font-style($size: 64px, $lineHeight: 69.63px, $color: #CD3C32);
    }

    h2 {
        margin-bottom: 24px;
        @include font-style($lineHeight: 43.52px);
        text-align: center;
    }

    p {
        @include font-style($weight: 400, $size: 20px, $lineHeight: 30px);
        text-align: center;
    }
}
</style>