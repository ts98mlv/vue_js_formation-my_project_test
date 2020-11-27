<template>
  <img alt="Vue logo" src="./assets/logo.png"><br>
  <input type="text" v-model="myVariable">
  <p v-if="show">{{myVariable}}</p>
  <p v-else>{{errorMsg}}</p>

  <input type="checkbox" name="check" id="check" v-model="show">
  <br>
  <ul>
    <li v-for="(element, index) in liste" v-bind:key="index">{{element}}</li>
  </ul>
  <br>
  <p>Liste d'objets</p>
  <ul>
    <li v-for="(element, index) in objectListe" v-bind:key="index" v-show="element.show" v-bind:style="{color : element.color}">{{index}}</li>
  </ul>

</template>

<script>


export default {
  name: 'App',
  data() {
    return{
      myVariable: undefined,
      show: false,
      errorMsg : "There is no variable",
      liste: ["Banane", "Kiwi", "Fraise"],
      objectListe:{
        "Banane" : {
            show: false,
          color: "yellow"
        },
        "Kiwi" : {
          show: true,
          color: "green"
        },
        "Fraise" : {
          show: true,
          color: "red"

        }
      }
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
