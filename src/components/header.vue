<template>
  <div id="app">
    <img src="../assets/logo.png">
   <h1> {{title}} </h1>
  </div>
</template>

<script>
export default {
  data(){
    return {
      title: ''
    }
  }
}

</script>

<style scoped>
*{
  color: rgb(236, 55, 55);
  background-color: #0A0A0A;
}
img{
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 30px;

}
</style>
