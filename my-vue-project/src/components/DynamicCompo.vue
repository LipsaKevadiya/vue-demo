<template>
<h2>Dynamic Component</h2>
<button  @click="tab='VueCompo'">Load VueCompo</button>
<button @click="tab='ReactCompo'">Load ReactCompo</button>
<button @click="tab='AngularCompo'">Load AngularCompo</button>
<!-- <VueCompo/>
<ReactCompo/>
<AngularCompo/> -->
<component :is="tab"/>
</template>

<script>
import VueCompo from './dynamic-compo/VueCompo.vue'
import ReactCompo from './dynamic-compo/ReactCompo.vue'
import AngularCompo from './dynamic-compo/AngularCompo.vue'
export default {
  name: 'DynamicCompo',
  components:{
    VueCompo,ReactCompo,AngularCompo
  },
  data(){
    return{
      tab:'VueCompo'
    }
  },


}
</script>

<style scoped>
h1 {
  color: orange
}
</style>