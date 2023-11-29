<script setup>
import FirstComponent from './components/FirstComponent.vue'
import MagicButton from './components/MagicButton.vue'
import Footer from './components/Footer.vue';

</script>

<template>
  <first-component title="My first Vue App" />
  <magic-button text="Dare click on me 😉" />
  <Footer />
</template>

<style scoped>
@import './assets/base.css';
@import './assets/main.css';
</style>
