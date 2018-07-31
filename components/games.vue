<template>
  <div class="row games" id=" app ">
    <ul>
      <li class="gAmE" :class="game.clas" v-for="game,index in games">
        <img :src="game.photo" alt="Game Images">
      </li>
    </ul>
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
      games: [
        {name:'Leauge Of Legends', photo: lol, show:'false', clas: 'lol'},
        {name: 'PUBG', photo: pubg, show:'false', clas: 'pubg'},
        {name: 'DOTA 2', photo: dota2, show:'false', clas: 'dota2'},
        {name: 'CS GO', photo: csgo, show:'false', clas: 'csgo'},
      ],
      activate_game: -1,
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

<style scoped>
.row{
  max-width: 1140px
}

ul{
  text-align: center;
}

.games{
  height: 387px;
  margin-left: 100px;
  margin-top: 50px;
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

.gAmE:focus {
  background-color: rgb(247, 85, 33);
}

.comeBack {

}
</style>
