<template>
  <div id="app">
    <h1>Animação CSS</h1>
    <Animation /> 
    <QuadToCircle />
  </div>
</template>

<script>
import Animation from './components/Animation';
import QuadToCircle from './components/Circle'

export default {
  name: 'App',
  components: {
    Animation,
    QuadToCircle
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
