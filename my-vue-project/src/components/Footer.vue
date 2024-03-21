<template>
<div class="footer">
<h2>Footer</h2>
<p>copy right @ {{ currentYear }}</p>
</div>

</template>

<script>
export default {
  name:'FooterCompo',
  data(){
    return{
     currentYear: new Date().getFullYear()
    }
  },

}
</script>

<style scoped>
.footer{
  color:orange;
  background-color: grey;
  position: absolute;
  bottom: 0;
  width: 100%;
}
</style>