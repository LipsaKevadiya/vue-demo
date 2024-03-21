<template>


<h2>beforeCreated and created lifecycle method {{name}}</h2>
</template>

<script>
export default {
  name:'CreateLifeCycle',
  data(){
    console.warn("data created");
    return{
     name:"lipsa"
    }
  },
  
  beforeCreate(){
      this.name="meet";
      alert("before created called");
    
  },
  created(){
    
    alert('created called');
  }
   
  
}
</script>
<style scoped>
h1{
  color:orange
}
</style>