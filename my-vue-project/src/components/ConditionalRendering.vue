<template>
<h1 v-if="show">if condition</h1>
<h1 v-else>else condition</h1>
<button v-on:click="show=!show">Click Me</button>

<h1>For loop</h1>
<ul>
<li v-for="item in names" :key="item">{{item}}</li>
</ul>

<ul>
  <li v-for="item in users" :key="item.email">Name: {{ item.name }} & Email: {{ item.email }}</li>
</ul>

</template>

<script>
export default {
  name: 'ConditionalRendering',
  data() {

    return {
      show: true,
      names:['lipsa','nency','isha','grinal'],
      users:[
        {
          name:"lipsa",
          email:"lipsa@gmail.com"
        },
         {
          name:"honey",
          email:"honey@gmail.com"
        },
         {
          name:"nency",
          email:"nency@gmail.com"
        },
      ]
    }
  },

}
</script>

<style scoped>
h1 {
  color: orange
}
</style>
