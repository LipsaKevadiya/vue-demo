<template>
<div class="user">
<h2>{{data.name}}</h2>
<h2>{{data.email}}</h2>
</div>

<button v-on:click="getData(data.name)">Alert Name</button>
</template>

<script>
export default {
  name: 'UserCompo',
  props: {

    data: Object,
    getData:Function 

  }
}
</script>

<style>
.user {
  color: black;
  background-color: skyBlue;
}
</style>
