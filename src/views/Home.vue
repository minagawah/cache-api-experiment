<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Hello" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // '@' is an alias to '/src'

export default Vue.extend({
  name: 'Home',
  components: {
    HelloWorld,
  },
});
</script>
