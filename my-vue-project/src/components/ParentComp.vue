<template>
<h2>Pass Data Child To Parent Component</h2>
<h2>{{childUser}}</h2>
<ChildComp :getUser="getUserName"/>
</template>


<script>
  import ChildComp from './ChildComp.vue'
  export default {
    name:'ParentComp',
    components:{
      ChildComp
    },
    data(){
      return{
        childUser:""
      }
    },
    methods:{
      getUserName(name){
        this.childUser = name
      }
    }
  }
</script>