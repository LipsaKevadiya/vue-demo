<template>

<h2>Reuse Component</h2>
<ul>

<li v-for="item in user" v-bind:key="item">
<ReuseChildCompo :data="item" :getData="getData"/>
</li>

</ul>

</template>

<script>
import ReuseChildCompo from './ReuseChildCompo.vue'
export default {
  name: 'ReuseParentCompo',
  components: {
    ReuseChildCompo
  },
  methods:{
    getData(name){
      alert(name);
    }
  },
  data() {
    return {
      user: [
        { name: "meet", email: "meet@gmail.com" },
        { name: "lipsa", email: "lipsa@gmail.com" },
         { name: "aesha", email: "aesha@gmail.com" },

      ]
     
    }
  },

}
</script>