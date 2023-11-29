<script>
export default {
  name: 'MagicButton',
  props: {
    text: {
      type: String,
      required: true,
      default: function () {
        return 'Click Me 😉'
      }
    }
  },
  data() {
    return {
      chiffre: 0,
      success: 'Coucou',
      sucessOne: 'Pas mal continu encore',
      sucessTwo: 'Tu te débrouille bien mais tu peux faire mieux !',
      sucessThree: 'Ca commence à être légendaire !!',
      sucessFour: "Bravo tu es maintenant sur d'être un sacrée dev qui sait cliquer"
    }
  },
  methods: {
    incrementation() {
      this.chiffre = this.chiffre + 1
      this.congrats()
    },

    congrats() {

    const box = document.querySelector('.success-container'); 

      if (this.chiffre > 10) {
        box.style.display='block'; 
        this.success = this.sucessOne
      }

      if (this.chiffre > 20) {
        this.success = this.sucessTwo
      }

      if (this.chiffre > 30) {
        this.success = this.sucessThree
      }

      if (this.chiffre > 40) {
        this.success = this.sucessFour
      }
    }
  }
}
</script>

<template>
  <div class="btn-container h-[50vh]">
    <button @click="incrementation">{{ text }}</button>
    <p class="number">{{ chiffre }}</p>
    <p class="success-container mb-12">{{ success }}</p>
  </div>
</template>

<style scoped>
button {
  background-color: green;
  color: white;
  border-radius: 25px;
  padding: 2em;
  font-size: 1.5em;
  border: none;
}

.btn-container {
  display: flex;
  justify-items: center;
  align-items: center;
  flex-direction: column;
  margin-top: 5em;
  gap: 3em;
}

.number {
  color: white;
}

.success-container {
  display: none;
  color: white;
  text-align: center;
  margin-top: 5em;
  background-color: green;
  padding: 1em;
  font-weight: bold;
  border-radius: 15px;
}
</style>
