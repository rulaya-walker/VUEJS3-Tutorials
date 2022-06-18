<template>
<div>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>

  <h2 v-bind:class="isSold ? 'sold-out' :'new'">Soldot ? movie</h2>

  <h2 v-bind:class="{
    promoted:isPromoted,
    new: !isSold,
    'sold-out':isSold
    }">Object Class Notation</h2>

  <h2 v-bind:style="{color:highlightColor,'font-size': highlightFont+'px'}">Incline Style</h2>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      name:"Sujata",
      isPromoted: true,
      isSold: true,
      highlightColor:'blue',
      highlightFont:50
      };
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

.promoted{
  font-style: italic;
}
.new{
  color: green;
}
.sold-out{
  color: red;
}
</style>
