<template>
<!-- <div><img v-bind:src="productImage"/></div> -->
<h2>Pass Data Parent To Child Component</h2>
<UserCompo name="lipsa kevadiya" :user="user" :getData="getData" :productImage="productImage" id="xyz"/>
</template>

<script>
import UserCompo from './UserCompo.vue'
export default {
  name: 'ParentCompo',
  components: {
    UserCompo
  },
  data() {
    return {
      user: { name: "meet", email: "meet@gmail.com" },
      productImage: require("../assets/panda.jpg")
    }
  },
  methods: {
    getData() {
      console.warn("parent function called");
      alert("parent function ")
    }
  }
}
</script>
