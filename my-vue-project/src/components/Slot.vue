<template>
<h1>Slots in vue js 3</h1>

<ChildCompo>
<template v-slot:header><h1 >Lipsa</h1></template>
<template v-slot:main><button>Click Me</button></template>
<template v-slot:footer><p>Mutiple slots with name</p></template>
</ChildCompo>

<ChildCompo>
<template v-slot:header><h1 >Meet</h1></template>
<template v-slot:main><button>Click Me</button></template>
<template v-slot:footer><p>Mutiple slots with name</p></template>
</ChildCompo>
<!-- <ChildCompo><h1>Html h1 tag</h1></ChildCompo>
<ChildCompo><a href="#">Link</a></ChildCompo> -->
</template>

<script>
import ChildCompo from './Child.vue'
export default {
  name: 'SlotCompo',
  components: {
    ChildCompo
  }


}
</script>

<style scoped>
h1 {
  color: orange
}
</style>
