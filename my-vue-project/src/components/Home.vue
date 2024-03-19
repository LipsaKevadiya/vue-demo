<template>
<h1>Home component {{"Hello".length}}</h1>
<h1>Email :{{email}}</h1>
<h1>mobile :{{mobile=8888}}</h1> 
<!-- we can also change value -->
<h1>name:{{getName("lipsa")}}</h1>
<h1>name:{{getVal("meet")}}</h1>
<h1>All Data:{{getData().email}}</h1>
</template>

<script>
export default {
  name:'HomeCompo',
  data(){
    return{
      email:'lipsaa@gmail.com',
      mobile:9999,
      getName:function(a){
        return a
      }
    }
  },
  methods:{
    getVal(name){
      return name
    },
    getData(){
      return{
        name:"lipsa",
        email:this.email
      }
    }
  }
}
</script>
<style scoped>
h1{
  color:orange
}
</style>