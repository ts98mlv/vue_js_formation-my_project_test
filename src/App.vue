<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <p>
    {{myVariable}}
  </p>
</template>

<script>


export default {
  name: 'App',
  data() {
    return{
      myVariable: "Hello World",
    }
  },
  mounted(){
    console.log(this.myVariable)
  },

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
