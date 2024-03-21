<template>

<h1>API Data</h1>

<ul class="item" v-for="item in list" :key="item.id">
<li>{{item.id}}</li>
<li>{{item.email}}</li>
<li>{{item.first_name}}</li>
<li><img :src="item.avatar"/></li>
</ul>



</template>

<script>
import axios from 'axios'
export default {
  name:'GetApiData',
  data(){
    return{
      list:[]
    }
  },
  async mounted(){
    let result = await axios.get("https://reqres.in/api/users?page=1");
    console.warn("api data", result.data.data)
    this.list = result.data.data;
  }

}
</script>

<style scoped>
h1{
  color:orange
}
.item{
  display:flex;
}
.item li{
  display:inline-block;
  width:180px;
  border: 1px solid;
  text-align:center;
  padding:5px;
}
</style>

