<template>
  <input v-model="message">
  <ProvideChildCompo />
</template>

<script>
import { ref, provide } from 'vue';
import ProvideChildCompo from './ProvideChildCompo.vue';

export default {
  name: 'ProvideInjectCompo',
  setup() {
    const message = ref('hello'); 

    provide('message', message);

  
    return {
      message
    };
  },
  components: {
    ProvideChildCompo
  }
}
</script>

