<template>
  <div id="app">
    <home/>
  </div>
</template>

<script>
import home from './components/pages/home.vue';

export default {
  name: 'app',
  components: {
    home
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
