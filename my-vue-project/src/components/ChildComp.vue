<template>

<h2>Child Component</h2>
<button v-on:click="getUser(UserName)">Send User Name</button>
</template>

<script>
  export default {
    name:'ChildComp',
    data(){
      return{
         UserName:"aesha",
      }
    },
    props:{
      getUser:Function,
    }
  }
</script>

<style >
h1{
  color:orange
}
</style>
