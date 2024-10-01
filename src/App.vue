<template>
  <!-- <h1>add methos -{{ add(5,3,20) }}</h1>
<h1>muilply methos -{{ muitply(45) }}</h1> -->
  <h1>{{ name }}</h1>
  <button @click="changeName, increment(2, $event)">change name</button>
  <h1>{{ counter }}</h1>
  <button @click="increment(5, $event)">increase</button>
  <button @click="decrement(5)">decrease</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // basenum:6
      name: "salam",
      counter: 0,
    };
  },
  methods: {
    //   add(x,y,z){
    //     return x+y+z;
    //   },
    //   muitply(num){
    // return  num*this.basenum
    //   }
    changeName() {
      return (this.name = "Hebras");
    },
    increment(num, event) {
      this.counter += num
      console.log(event)
    },
    decrement(num) {
      this.counter -= num;
    },
  },
};
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
