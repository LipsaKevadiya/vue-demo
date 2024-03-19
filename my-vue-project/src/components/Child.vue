<template>
<div class="cart">

<header>
<slot name="header">default value</slot>
</header>

<content>
<slot name="main">default value</slot>
</content>

<footer>
<slot name="footer">default value</slot>
</footer>
</div>
</template>

<script>
export default{
  name:'ChildCompo',

}
</script>

<style scoped>
.cart {
  border: 1px solid;
  width: 170px;
}
</style>