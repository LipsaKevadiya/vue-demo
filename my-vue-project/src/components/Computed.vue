<template>
<h1>Computed property</h1>
<h1>{{(doller*rupeeVal)-discount}}</h1>
<h1>{{(doller*rupeeVal)-discount}}</h1>
<h1>{{getResult}}</h1>
</template>

<script>
export default {
  name:'ComputedProperty',
  data(){
    return{
      doller:100,
      rupeeVal:70,
      discount:10,
    }
  },
  computed:{
    getResult(){
      return (this.doller*this.rupeeVal)-this.discount;
    }
  },
}
</script>
<style scoped>
h1{
  color:orange
}
</style>