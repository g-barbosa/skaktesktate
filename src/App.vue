<template>
  <div id="app">
    <div >
      <div class="audio">
        <audio  autoplay loop controls>
          <source src="./assets/daasdsdd.mp3" type="audio/mp3">
        </audio>   
      </div>

      <div class="images">
        <img   v-if="step == 0" src="./assets/skate/dasdasd1.png">
        <img  v-if="step == 1" src="./assets/skate/andando.gif">
        <img   v-if="step == 2" src="./assets/skate/tudo.gif">
      </div> 

      <div class="buttons">
        <button v-if="step == 1"   v-on:click="step = 0"> parar</button>
        <button v-if="step == 0"   v-on:click="step = 1">remar</button>
        <button   v-if="step != 2" :disabled="step == 0" v-on:click="step = 2">se empolgar</button>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data:() => ({
    step: 0
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

img{
  width: 200px
}
html{
  background-color: black
}

</style>
