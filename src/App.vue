<template>
  <div id="app">
    <LogIn/>
  </div>
</template>

<script>
import LogIn from './components/LogIn.vue'

export default {
  name: 'App',
  components: {
    LogIn
  }
}
</script>

<style>
  #app {
    margin: 0;
    padding: 0;
    font-family: Nunito;
  }
</style>
