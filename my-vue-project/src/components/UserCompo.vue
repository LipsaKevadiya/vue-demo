<template>
<!-- To bind id from parent component -->
<div v-bind="$attrs">

  <img :src="productImage" />
</div>
<h2>{{name}}</h2>
<h2>{{user.name}}</h2>
<button v-on:click="getData()">getData</button>
</template>

<script>
export default {
  name: 'UserCompo',
  props: {
    name: String,
    user: Object,
    getData: Function,
    productImage: String
  }
}
</script>

<style>
h1 {
  color: orange
}
</style>
