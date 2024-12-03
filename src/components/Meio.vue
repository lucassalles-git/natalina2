<script setup>
import presentes from "../assets/presentes.png"
</script>

<template>
    <main>
        <section class="tempo-limitado">
            <div>
                <h2>Tempo limitado</h2>

                <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.
                </p>
            </div>
            <img :src="presentes" alt="">
        </section>
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
    border: solid;
    padding: 80px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;

    div{
        width: 477px;
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