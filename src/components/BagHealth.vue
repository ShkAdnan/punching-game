<template>
  <div class="bag-health">
    <div v-bind:style="{width : health + '%'}"></div>
  </div>
</template>

<script>
export default {
  name: 'BagHealth',
   props : ['health']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.bag-health{
    width: 200px;
    border: 2px solid #000;
    margin: 0 auto 20px auto;
}
.bag-health div{
   height: 20px;
   background :crimson;
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
