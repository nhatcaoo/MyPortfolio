<template>

  <div id = 'app'>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Sudoku />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Sudoku from './components/Sudoku'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Sudoku,
  }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
    font-family: Poppins;
    color:white;
}
#app {
 
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;

}
</style>
