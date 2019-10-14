<template>
 <div class="message">
      <p>{{greetings}}</p>

      <input type="text" v-model="firstName" v-on:keydown.enter="displayGreetings=false"/>
      <p v-if="firstName">Ah ! Je me souviens de toi ! Bonjour {{firstName}} !</p>
    </div>
</template>

<script>
export default{
data(){
    return { 
      greetings:"Hé ! Bonjour quel est ton nom?",
      firstName:"", 
      displayGreetings:true};
  },
};
</script>

<style scoped>

</style>