<template>
<h2>Use of Composition api</h2>
<h2>{{Topic}}</h2>
<h2>{{formData.age}}</h2>

</template>


<script>
import {ref , reactive } from 'vue'
  export default {
    name:'CompositionComp',
   
    setup(){
        const Topic = ref("test composition ")
        const formData = reactive({
          name:"lipsa",
          age:"22"
        })
        setTimeout(() => {
          Topic.value='00000'
        }, 2000);
        return {
          Topic,
          formData
        }
    },
   
  }
</script>