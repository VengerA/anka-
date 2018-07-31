<template>
  <div id="app" class="">
    <div class="button_seat">
      <button class="btn-ghost" type="button" name="button" v-show="!showseats" v-on:click="showseats = !showseats">Degistir</button>
    </div>
    <div class="seats" v-show="showseats">
      <div class="queue" v-for="queue in queues">
        <div class="seats">
          <ul>
            <li class="seat" v-for="seat in seats">
              <button>
                <ion-icon name="tv"></ion-icon>
              </button>
            </li>
          </ul>
        </div>
        <div class="seats ">
          <ul>
            <li  class="seat " v-for="seat in seats">
              <button>
                <ion-icon name="tv"></ion-icon>
              </button>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="next">
      <button class="btn-ghost" type="button" v-show="showseats" v-on:click="showseats = !showseats, showing_payment">Ileri</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
        seats:[1, 2, 3, 4,],
        queues:[1, 2],
        showseats: false
    }
  }
}

</script>

<style>
.seats {
  width: 37.5%;
  float: left;
}

.seat{
  font-size: 40px;
  padding-left: 0;
  color: black;
  margin-bottom: 10px;
  float: left;
  width: 9.375;
}

.seat:hover {
  color: #e94f62;
  -webkit-transition: 1s;
}

.btn-ghost {
  display: inline-block;
  border: 2px solid rgb(6, 6, 3);
  background-color: #fff;
  border-radius: 20px;
  font-size: 19px;
}

.btn-ghost:hover {

}

</style>
