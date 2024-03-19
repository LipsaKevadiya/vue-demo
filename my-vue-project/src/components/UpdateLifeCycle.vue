<template>


<h2>beforeUpdated and updated lifecycle method {{name}}</h2>
<h1 ref="count">{{counter}}</h1>
<button v-on:click="counter=counter+1">Click Me</button>
</template>

<script>
export default {
  name:'UpdateLifeCycle',
  data(){
   
    return{
     counter:0
    }
  },
  
  beforeUpdate(){
      console.log("beforeUpdate", this.$refs['count'].textContent);
    
  },
  updated(){
    
    console.log("Updated", this.$refs['count'].textContent);
  }
   
  
}
</script>
<style scoped>
h1{
  color:orange
}
</style>