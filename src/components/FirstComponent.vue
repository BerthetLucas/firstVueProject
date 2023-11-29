<script>

export default {
  name: 'FirstComponent',
  props: {
    title: {
      type: String,
      required: true,
      default: function () {
        return 'First Vue application'
      }
    }
  }
}
</script>

<template>
  <h1 class="">{{title}}</h1>
</template>

<style scoped>
h1 {
  color: green;
  text-align: center;
}
</style>
