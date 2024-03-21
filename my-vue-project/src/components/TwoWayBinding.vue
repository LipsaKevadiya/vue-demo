<template>
  
    <h1>Two way binding</h1>
    <input type="text"  v-model.lazy.trim="count"/>
    
    <h1>{{count}}</h1>
 
</template>

<script>
export default {
  name: 'TwoWayBinding',
  data(){
    return{
      count:100
    }
  }
 
}
</script>

<style scoped>
h1{
  color:black
}
</style>