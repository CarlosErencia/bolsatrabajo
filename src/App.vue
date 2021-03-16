<template>
  <div id="app">
    <Botones/>
  </div>
</template>

<script>
import Botones from './components/Botones.vue'

export default {
  name: 'App',
  components: {
    Botones
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
