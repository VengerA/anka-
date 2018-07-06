<template>
  <div class="row col span-1-of-3" id=" app ">
    <h1> {{title}}</h1>
    <ul>
      <li class="gAmE" v-for="game,index in games" v-on:click="" v-if="activate_game == index">
        <img src="game.photo" alt="Game Images">
        <h2>{{game.name}}</h2>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      games: [
        {name:'Leauge Of Legends', photo:'./img/lol.jpg', show:'false'},
        {name: 'PUBG', photo:'./img/PUBG.jpg', show:'false'},
        {name: 'DOTA 2', photo:'./img/Dota2.jpg', show:'false'},
        {name: 'CS GO', photo:'./img/csgo.jpg', show:'false'},
      ],
      activate_game: 0,
    }
  }
}

</script>

<style scoped>
  .row{
    max-width: 1140px
  }
  h1{
    color: green;
  }
</style>
