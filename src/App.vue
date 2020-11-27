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
    <li v-bind:class="{'bgColor' : element.bgGrey}" v-for="(element, index) in objectListe" v-bind:key="index" v-show="element.show">{{index}}</li>
  </ul>
  
  <div id="fonctions">
    <label for="clog">Console log : </label>
    <input type="text" id="clog" @input="logThis" v-model="cloged">

    <br><button name="clickMe" @click="clickedButton">Click me !</button>
    <p>{{count}}</p>
  </div>

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
            bgGrey: true
        },
        "Kiwi" : {
          show: true,
          bgGrey: false
        },
        "Fraise" : {
          show: true,
          bgGrey: true

        }
      },
      cloged : undefined,
      clickedbuttonValue: "Hello World",
      count : 0
    }
  },
  methods: {
    logThis(){
      console.log(this.cloged)
    },
    clickedButton(){
      console.log(this.clickedbuttonValue);
      this.counting();
    },
    counting(){
      this.count ++
    }
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
