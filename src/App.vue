<template>
  <img alt="Vue logo" src="./assets/logo.png"><br>
  <Home></Home>

</template>

<script>
import Home from "./views/Home";

export default {
  name: 'App',
  components:{
    Home,
  },
  data() {
    return{

    }
  },
  methods: {

  },
  computed: {

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

.bgColor{
  background-color: grey;
}
</style>
