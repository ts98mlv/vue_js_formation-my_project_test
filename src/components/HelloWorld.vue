<template lang="html">
  <div>
    <h1>Hello World !</h1>
    <h3>{{message}}</h3>

    <ul>
      <li v-for="(element, index) in myArray" :key="index">{{element}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props:{
    message: String,
    myArray : Array
  }
}
</script>

<style scoped>

</style>