<template>
  <div class="controller">
    <button v-on:click="punch" v-show="!ended">PUNCH</button>
    <button v-on:click="restart">RESTART</button>
  </div>
</template>

<script>
export default {
  name: 'GameController',
  data(){
    return {
      health : 100,
      ended  : false
    }
  },
  methods : {
    punch(){
      this.health -= 10;
      if(this.health <= 0) this.ended = true;
      this.$emit('health', this.health)
      this.$emit('ended', this.ended)
    },
    restart(){
      this.health = 100;
      this.ended = false;
      this.$emit('health', this.health)
      this.$emit('ended', this.ended)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
