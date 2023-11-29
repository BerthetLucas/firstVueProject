<script setup>
import FirstComponent from './components/FirstComponent.vue'
import MagicButton from './components/MagicButton.vue'
import Footer from './components/Footer.vue';

</script>

<template>
  <div class="flex flex-col justify-center items-center">
  <first-component title="My first Vue App" />
  <magic-button text="Dare click on me 😉" />
  <Footer />
</div>
</template>

<style scoped>

</style>
