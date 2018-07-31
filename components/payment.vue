<template>
  <div id="app">
    <div class="accordion3">
      <a v-show="!showPayment" v-on:click="showPayment">Odeme Zamanı</a>
    </div>
    <div v-show="showPayment" class="paymentScreen">
      <h1>Buraya Odeme Ekranı Gelecek</h1>
      <button type="button" name="button">Ileri</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      showPayment: false
    }
  }
}

</script>

<style scoped>

</style>
