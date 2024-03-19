<template>
<h2>Pass Data Parent To Child Component</h2>
<UserCompo name="lipsa kevadiya" :user="user" :getData="getData"/>
</template>

<script>
  import UserCompo from './UserCompo.vue'
  export default {
    name:'ParentCompo',
    components:{
      UserCompo
    },
    data(){
      return{
        user:{name:"meet",email:"meet@gmail.com"}
      }
    },
    methods:{
      getData(){
        console.warn("parent function called");
        alert("parent function ")
      }
    }
  }
</script>