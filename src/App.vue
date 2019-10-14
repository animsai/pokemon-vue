<template>
  <div id="app" class="display">
    <img alt="Pallet town" src="./assets/pallettown.png">
    <Sacha/>
    <div class="message">
      <p>{{greetings}}</p>

      <input type="text" v-model="firstName" v-on:keydown.enter="displayGreetings=false"/>
      <p v-if="firstName">Ah ! Je me souviens de toi ! Bonjour {{firstName}} !</p>
    </div>
  </div>
</template>

<script>
import Sacha from '/components/Sacha.vue';

export default {
  data(){
    return { 
      greetings:"Hé ! Bonjour quel est ton nom?",
      firstName:"", 
      displayGreetings:true};
  },
  name: 'app',
  components: {
    Sacha,
  }
}
</script>

<style>
img {
  width:800px;
  margin-left:2px;
  image-rendering:pixelated;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
