<script setup>
import logo from "../assets/logo.png"
import antigoTwitter from "../assets/antigoTwitter.png"
import whatsApp from "../assets/whatsApp.png"
import instagram from "../assets/instagram.png"
import facebook from "../assets/facebook.png"
import google from "../assets/google.png"
</script>

<template>
    <footer>
        <img :src="logo" alt="">

        <div class="social">
            <img :src="antigoTwitter" alt="">
            <img :src="whatsApp" alt="">
            <img :src="instagram" alt="">
            <img :src="facebook" alt="">
            <img :src="google" alt="">
        </div>
    </footer>
</template>

<style scoped lang="scss">
footer {
    padding: 20px 352px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    background-color: #FFE9E8;

    @media (max-width: 440px) and (max-height: 956px) {
        height: 222px;
        padding: 0;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 32px;
    }
}

.social {
    display: flex;
    gap: 36px;

    @media (max-width: 440px) and (max-height: 956px) {
        gap: 8vw;
    }
}
</style>