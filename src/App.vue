<template>
  <h2>Volume Tracker 0 -20</h2>
  <h2>Current Volume - {{ volume }}</h2>
  <div>
    <button @click="volume +=2">Increase</button>
    <button @click="volume -=2">Decrease</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      volume: 0
      }
      
  },
  methods:{},
  computed:{},
  watch:{
    volume(newValue,oldValue){
      if(newValue > oldValue && newValue === 16){
        alert('Listening to hight volume is damamage for hearing');
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
div{
  display: block;
  width: 70%;
  margin: 0 auto;
  margin-top: 25px;
}



</style>
