<template>
  <div id="app">
    <h1> {{title}} </h1>
    <app-games></app-games>
  </div>
</template>

<script>
import Games from './components/games.vue'
import seats from './components/seats.vue'
export default {
  components: {
    'app-games': Games,
    'app-seats': seats,
  },
  data(){
    return {
      title: 'Ufuk Adamdir'
    }
  }
}

</script>

<style>

</style>
