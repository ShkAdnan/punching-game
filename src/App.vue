<template>
  <BagImage :ended="ended"/>
  <BagHealth :health="health"/>
  <GameController v-on:health="healthFunc($event)" v-on:ended="endedFunc($event)"/>
</template>

<script>
import BagImage from './components/BagImage.vue';
import BagHealth from './components/BagHealth.vue';
import GameController from './components/GameController.vue';

export default {
  name: 'App',
  components: {
    BagImage,
    BagHealth,
    GameController
  },
  data(){
    return {
      health : 100,
      ended  : false
    }
  },
  methods : {
    healthFunc(value){
      this.health = value;
    },
    endedFunc(value){
      this.ended = value;
    }
  }
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
</style>
