<template>
  <div id="app" class="display">
    <Scene/>
    <Sacha v-if="displaySacha"/>
    <Greetings v-on:greetingsFinished="displaySacha"/>
  </div>
</template>

<script>
import Sacha from './components/Sacha.vue';
import Scene from './components/Scene.vue';
import Greetings from './components/Greetings.vue';

export default {
 
  name: 'app',
  components: {
    Scene,
    Sacha,
    Greetings
    
  },
  data(){
    return {
      displaySacha:false;
    }
  }
}
</script>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
