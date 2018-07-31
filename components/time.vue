<template>
  <div class="time" id="app">
    <div class="changeTime">
      <button type="button" v-show="!showingsituation" v-on:click="showingsituation = !showingsituation">Degistir</button>
    </div>
    <div class="timeShowed" v-show="showingsituation">
          <h1>Buraya Zaman SEcim Ekrani Gelicek</h1>
    </div>
    <div class="nextTime" v-show="showingsituation">
      <button type="button" v-on:click="showingsituation = !showingsituation">Ileri</button>
    </div>
  </div>

</template>

<script>
export default {
  data(){
    return{
      showingsituation: true
    }
  }
}
</script>

<style scoped>

.time {
  margin-left: 100px;
  margin-top: 50px;
  float: left;
}

.row{
  max-width: 1140px
}
</style>
