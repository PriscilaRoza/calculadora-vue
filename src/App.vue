<template>
  <div id="app">
    <Calculadora/>
  </div>
</template>

<script>
// eslint-disable-next-line import/extensions
import Calculadora from './components/Calculadora.vue';

export default {
  name: 'App',
  components: {
    Calculadora,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-image: url('https://static8.depositphotos.com/1006106/892/v/600/depositphotos_8921462-stock-illustration-physics.jpg');
  width: 100vw;
  height: 100vh;
  background-repeat:cover;
  position: fixed;
    left: 0;
    right: 0;
    z-index: 1;
}
*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}
</style>
