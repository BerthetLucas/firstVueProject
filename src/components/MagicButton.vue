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
        chiffre: 0
    }
  },
  methods: {
    incrementation() {
        console.log("deef")
        this.chiffre = this.chiffre + 1 
    }
  }
}
</script>

<template>
<div class="btn-container">
  <button @click="incrementation">{{ text }}</button>
  <p class="number">{{chiffre}}</p>
</div>


</template>

<style scoped>
button {
    background-color: green;
    color : white; 
    border-radius : 25px; 
    padding : 2em; 
    font-size : 1.5em; 
    border : none; 
}

.btn-container {
    display: flex;
    justify-items: center;
    align-items: center;
    flex-direction: column;
    margin-top: 5em; 
    gap : 3em; 
}

.number {
    color : white;
}

</style>
