<template>
    <h1>get value of checkbox</h1>
    <h1>Selected Tech:{{ technology }}</h1>
    <lable for="js">JavaScript</lable>
    <input type="checkbox" value="js" id="js" v-model="technology"/>
     <lable for="React">React</lable>
    <input type="checkbox" value="React" id="React" v-model="technology"/>
     <lable for="Vue">Vue</lable>
    <input type="checkbox" value="Vue" id="Vue" v-model="technology"/>
    
    <h1>get value of radio button</h1>
    <h1>Selected Tech:{{ tech }}</h1>
    <lable for="js">JavaScript</lable>
    <input type="radio" value="js" id="js" v-model="technology"/>
     <lable for="React">React</lable>
    <input type="radio" value="React" id="React" v-model="technology"/>
</template>

<script>
export default {
  name: 'GetValue',
  data(){
    return{
      technology:[],
      
    }
  }
}
</script>

<style scoped>
h1{
  color:black
}
</style>