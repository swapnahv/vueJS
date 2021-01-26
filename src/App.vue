<template>
  
  <div>
    <LoadCard msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import LoadCard from './components/LoadCard.vue';

export default {
  name: 'App',
  data() {
    return {
    }
  },
  components: {
    LoadCard,
  }
}
</script>

<style>
  @import './app.scss';
</style>
