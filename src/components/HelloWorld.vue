<script>

import SousComposant from './SousComposant.vue'; 

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
  name: 'HelloWord',
  props: {
    msg: {
      type: [String, Number, Object],
      required: true,
      default: function () {
        return 'Coucou'
      }
    },
    visibility: {
      type: Boolean,
      required: false,
      default: function () {
        return true
      }
    },
    data() {
      return { count: 0 }
    }
  }
}


</script>

<template>
  <div class="greetings">
    <h1 class="green" v-if="visibility">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
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
