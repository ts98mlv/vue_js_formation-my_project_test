<template>
  <img alt="Vue logo" src="./assets/logo.png"><br>
  <input type="text" v-model="myVariable">
  <p>{{myVariable}}</p>
</template>

<script>


export default {
  name: 'App',
  data() {
    return{
      myVariable: undefined,
    }
  },
/*  mounted(){
    console.log(this.myVariable)
  },*/

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
