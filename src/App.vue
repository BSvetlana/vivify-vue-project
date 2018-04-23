<template>
  <div id="app">
    <ContanctsList/>
  </div>
</template>

<script>
import ContanctsList from './components/ContanctsList.vue'

export default {
  name: 'app',
  components: {
      ContanctsList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
