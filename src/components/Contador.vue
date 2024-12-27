<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import presentes from "../assets/presentes.png";

const targetDate = new Date(new Date().getFullYear(), 11, 25);
const timeRemaining = ref(null);
let timer = null;

const updateTimer = () => {
  const now = new Date();
  const difference = targetDate - now;

  if (difference <= 0) {
    clearInterval(timer);
    timeRemaining.value = null;
    return;
  }

  const days = Math.floor(difference / (1000 * 60 * 60 * 24));
  const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((difference % (1000 * 60)) / 1000);

  timeRemaining.value = { days, hours, minutes, seconds };
};

onMounted(() => {
  updateTimer();
  timer = setInterval(updateTimer, 1000);
});

onBeforeUnmount(() => {
  clearInterval(timer);
});
</script>

<template>
      <div class="cronometro">
      <p v-if="timeRemaining">
        {{ timeRemaining.days }} d-
        {{ timeRemaining.hours }} h-
        {{ timeRemaining.minutes }} m-
        {{ timeRemaining.seconds }} s
      </p>
      <p v-else>Feliz Natal!! 🎄</p>
    </div>
</template>

<style scoped lang="sass">
</style>