<script>
// defineProps({
//   msg: {
//     // On peut assigner plus types : type: [String, Number];
//     type: String,
//     required: true
//     //On peut ajouter une valeur par défaut :
//     // default: null
//   }
// })

export default {
  name: 'SousComposant',
  props: {
    msg: {
      type: String,
      required: true,
      default: function () {
        return 'Coucou je suis le sous composant'
      }
    },

    data() {
      return
    }
  }
}
</script>

<template>

<p>
    {{ msg }}
</p>



</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
