<template>
  <div id="app" class="row">
    <div class="games row">
      <ul>
        <li class="gAmE" :class="game.clas" v-on:click v-for="game,index in games">
          <img :src="game.photo" alt="Game Images">
        </li>
      </ul>
    </div>
    <div class="que1 row">
      <div class="comers">
        <label>Kac Kisi Geliceksiniz</label>
      </div>
      <div class="addingPeople row">
        <div class="remover" v-on:click="comingPeople = comingPeople - 1">
            <a class="btn_2">
              <ion-icon name="remove"></ion-icon>
            </a>
        </div>
        <div class="coming_people row">
          <p>{{comingPeople}}</p>
        </div>
        <div class="adder" v-on:click="comingPeople ++">
          <a class="btn_2">
            <ion-icon name="add"></ion-icon>
        </a>
        </div>
      </div>
      <div class="sira">
        <p class="siradaki1"> Ufuk Adlı <br> 4 kişi <br>Yaklaşık 30 dakika</p>
        <p class="siradaki2"> Aslan Parcasi <br> 2 kişi <br>Yaklaşık 45 dakika</p>

      </div>
    </div>
    <div class="row desksNear">
      <div class="contentNear">
        <label>Masalarin yan yana olmasini istiyorum</label>
        <p>(Yer bulmasi daha uzun surer)</p>
      </div>
      <div class="checkBox" v-on:click="show_onay = !show_onay">
        <img v-show="show_onay" src="../assets/onay.png">
      </div>
    </div>
    <div class="row enterQue">
      <a class="enterQue1" type="button" name="button" v-on:click="resetTheFloor, comingPeople = 0">Siraya gir</a>
    </div>
  </div>
</template>

<script>
import lol from "../assets/lol.png"
import pubg from "../assets/pubg.png"
import dota2 from "../assets/dota2.png"
import csgo from "../assets/csgo.png"

export default {
  data(){
    return {
      title: 'Siraya GirMek icin Asagidaki/ Asamalari Hallet It',
      comingPeople: 0,
      games: [
        {name:'Leauge Of Legends', photo: lol, show:'false', clas: 'lol'},
        {name: 'PUBG', photo: pubg, show:'false', clas: 'pubg'},
        {name: 'DOTA 2', photo: dota2, show:'false', clas: 'dota2'},
        {name: 'CS GO', photo: csgo, show:'false', clas: 'csgo'},
      ],
      activate_game: -1,
      change_game: false,
      show_onay: false
    }
  },
  methods: {
    select_game(index){
      this.activate_game = index

    },
    resetTheFloor(){
      this.activate_game = -1
    }
  }
}
</script>

<style>

.games{
  height: 387px;
  margin-left: 100px;
  margin-top: 50px;
  float: left;
  margin-bottom: -200px;
}

.gAmE{
  float: left;
  width: 18.75%;
  display: inline-block;
  border: 3px solid #ff0000;
  height: 100px;
  width: 260px;
  padding-top: 20px;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

.gAmE:hover {
  background-color: rgb(247, 85, 33);
  -webkit-transition: background-color 0.5s, border 0.5s, color 0.5s;
}

.changeGame{
  margin-left: 50px;
  display: inline-block;
  padding: 10px 40px;
  font-weight: 400;
  text-decoration: none;
  border-radius: 20px;
  border: 0.6px solid ;
  color: #e02f2f;
  background-color: #0A0A0A;
}

.changeGame:hover {
    background-color: #282828;
    color: rgb(236, 236, 234);
}

.que1 {
  margin-left: 250px;
  width: 75%;
  float: left;
}

.makeQue{
  float: left;
  width: 56.25%;
}

.comers {
  margin-left: -50px;
  font-size: 25px;
  float: left;
  width: 30%;
  margin-right: -60px;
}

.addingPeople {
  float: left;
  width: 16.25%;
  margin-left: 100px;
  margin-top: 8px;
}

.adder {
  float: left;
  width: 8%;
  margin-left: 40px;
  font-size: 30px;
  margin-top: -5px;
  -webkit-transition: background-color 0.2s, border 0.2s, color 0.2s;
}

.coming_people {
  width: 9.25%;
  float: left;
  margin-left: 60px;
  margin-top: -55px;
  font-size: 40px;
}

.remover {
  float: left;
  width: 8%;
  font-size: 30px;
  margin-top: -5px;
}

.remover:hover,
.adder:hover {
  color: #ff0000;
}

.sira {
  margin-left: 50px;
  background-color: rgb(61, 59, 59);
  border-radius: 30px;
  height: 250px;
  float: left;
  width: 18.75;
  width: 300px;
  text-align: center;
}

.siradaki1 {
  display: inline-block;
  border-radius: 30px;
  background-color: rgb(54, 54, 54);
  width: 250px;
  height: 80px;
  padding-top: 15px;
  margin-top: 20px;
}

.siradaki2 {
  display: inline-block;
  border-radius: 30px;
  background-color: rgb(54, 54, 54);
  width: 250px;
  height: 80px;
  padding-top: 15px;
  margin-top: -1px;
}

.desksNear {
  float: left;
  width: 30%;
  margin-left: 140px;
  margin-top: -150px;
  text-align: center;
  margin-right: 300px;
}

.checkBox {
  float: left;
  width: 40px;
  background-color: white;
  height: 40px;
  border: 2px solid #e02f2f;
  border-radius: 10px;
  margin-left: 480px;
  margin-top: -65px;
  -webkit-transition: background-color 0.2s, border 0.2s, color 0.2s;
}

.checkBox:hover {
  background-color: rgb(254, 114, 114);
}

.enterQue {
  float: left;
  margin-left: 350px;
  display: inline-block;
  border: 1px solid #F00;
  text-decoration: none;
  padding-left: 20px;
  padding-right: 20px;
  border-radius: 10px;
  padding-top: 20px;
  padding-bottom: 20px;
  font-size: 20px;
  -webkit-transition: background-color 0.2s, border 0.2s, color 0.2s;
}

.enterQue:hover {
  background-color: rgb(255, 255, 255);
  color: #0B0B0B;
}

</style>
