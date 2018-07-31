<template>
  <div id="app">
    <div class="all">
      <div class="header row">
          <app-header></app-header>
      </div>
      <div class="buttons_enter ">
        <div class="enterence_buttons row">
          <a class="btn btn_full" v-on:click="show_que = !show_que, show_randevu = false">
            <p class="inButton">Siraya<br> Gir</p>
          </a>
          <br>
          <a class="btn btn_ghost" v-on:click="show_randevu = !show_randevu, show_que = false">
            <p class="inButton">Randevu<br> Al</p>
          </a>
        </div>
      </div>
      <div class="components_enter">
        <div class="randevu row" v-show="show_randevu">
          <app-games class=""></app-games>
          <app-time class=""></app-time>
          <app-seats class=""></app-seats>
          <app-payment class=""></app-payment>
        </div>
        <div class="que" v-show="show_que">
          <app-que></app-que>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Games from './components/games.vue'
import seats from './components/seats.vue'
import time from './components/time.vue'
import header from './components/header.vue'
import que from './components/que.vue'
import payment from './components/payment.vue'

export default {
  components: {
    'app-games': Games,
    'app-seats': seats,
    'app-time' : time,
    'app-header': header,
    'app-que': que,
    'app-payment': payment
  },
  data(){
    return {
      show_randevu: false,
      show_que: false,
    }
  },
  methods: {
    showing_payment(){
      showPayment = !showPayment
    }
  }
}

</script>

<style>
.all {
  background-color: #0A0A0A;
  background-position: center;
  height: 300vh;
  background-attachment: fixed;
  font-family: 'Orbitron', sans-serif;
  color: rgb(218, 218, 221);
}

.buttons_enter {
  float: left;
  width: 25%
}

.components_enter{
  float: left;
  width: 75%
}



/*------BUTTONS------*/

.btn{
  font-size:30px;
    height: 180px;
    width: 180px;
    border-radius: 50%;
    margin-top: 50px;
    margin-left: 300px;
    -webkit-transition: background-color 0.5s, border 0.5s, color 0.5s;
}

.btn_full{
  display: inline-block;
  text-decoration: none;
  border: 3px  solid #ff0000;
  color: #ff0000;
  background-color: #0B0B0B;
}

.btn_full:hover {
  background-color: #282828;
  color: #e02f2f;
}

.btn_ghost{
  display: inline-block;
  font-weight: 400;
  text-decoration: none;
  border: 3px solid #ff0000;
  color: #ff0000;
  background-color: #0A0A0A;
}

.btn_ghost:hover {
    background-color: #282828;
    color: rgb(236, 236, 234);
}

.inButton{
  padding-left: 5px;
  padding-top: 30px;
  text-align: center;
}

/*-------Reusable components ------*/


</style>
