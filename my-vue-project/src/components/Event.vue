<template>
<h1 v-on:mousemove="getConsole()">Home component </h1>
<button v-on:click="getData()">Click Me</button>
<button v-on:dblclick="getData('button double clicked')">Click Me</button>
<h2>{{count}}</h2>
</template>

<script>
export default {
  name:'EventCompo',
  data(){
    return{
      count:0
    }
  },
  methods:{
    getData(){
      
        this.count=this.count+1;
      
    },
    getConsole(){
      console.warn('function called')
    }
   
  }
}
</script>
<style scoped>
h1{
  color:orange
}
</style>