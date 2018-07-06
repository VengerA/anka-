<template>
  <div class="first row col span-1-of-3" id=" app " v>
    <button v-on:click="myFunction" type="button">Devam Et</button>
  </div>
</template>

<script>
export default {
  data: function(){
    return {
      x = document.getElementsByClassName('first');
    }
  }
  methods:{
    function myFunction() {
      if (this.$data.x.style.display === "none") {
          this.$data.x.style.display = "block";
        } else {
          this.$data.x.style.display = "none";
        }
      }
    }
  }
}

</script>

<style scoped>
  .row{
    max-width: 1140px
  }
</style>
