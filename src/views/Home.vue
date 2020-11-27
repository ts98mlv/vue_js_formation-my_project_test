<template lang="html">
  <div id="home">
    <p>home</p>

    <HelloWorld message="Thomas" :myArray="myArray"></HelloWorld>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld";

export default {
  name: "Home",
  components:{
    HelloWorld
  },
  data() {
    return{
      myArray : ["Banane", "Kiwi", "Fraise"],
    }
  },
}
</script>

<style scoped>

</style>