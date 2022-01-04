<template>
  <div class="bag" v-bind:class="{burst : ended}">
  
  </div>
</template>

<script>
export default {
  name: 'BagImage',
  props : ['ended']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bag {
  width: 200px;
  height: 500px;
  margin: 0 auto;
  background : url(../assets/bag.png) center no-repeat;
  background-size: 80%;
}
.bag.burst {
  background : url(../assets/bag-burst.png) center no-repeat;
  background-size: 80%;
}
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
