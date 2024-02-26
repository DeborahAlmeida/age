<template>
  <CalculadoraIdade />
</template>

<script>
import CalculadoraIdade from './components/CalculadoraIdade.vue'

export default {
  name: 'App',
  components: {
    CalculadoraIdade
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  border:2px solid blue;
  width:100vw;
  height:100vh;
  background-color: blue;
}
</style>
