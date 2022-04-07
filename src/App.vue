<template>
  <div id="app">
    <h2> {{ name }} </h2>
  <div>
    <button @click="changeName" > Change Name !</button>
  </div>


  <h2>{{ count }}</h2>
<!-- with inline methods -->
  <!-- <div>
    <button v-on:click="count++" >Increment</button>
    <button v-on:click="count--" >Decrement</button>
  </div> -->

  <!-- with methods -->
  <div>
    <button @click="increment(2, $event)" >Increment</button>
    <button @click="decrement(2)" >Decrement</button>
  </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
      name: 'kavin sebastian',
      count: 0
    }
  },
  methods:{
    increment(num, event){
      this.count += num
      console.log(event.target)
    },
    decrement(){
      this.count -= 1
    },
    changeName(e){
      console.log(e)
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
