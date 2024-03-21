<template>

<h2>Teleport Compo</h2>

<teleport to="#footer">
<h1>HTML Content</h1>
<FooterCompo/>
</teleport>


</template>

<script>
import FooterCompo from './Footer.vue'
export default {
  name: 'TeleportCompo',
  components: {
    FooterCompo
  },
  

}
</script>