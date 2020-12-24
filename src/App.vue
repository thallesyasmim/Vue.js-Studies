<template>
  <div id="app">
    <h1>CSS Animation</h1>
    <Animation /> 
    <QuadToCircle />
    <Footer />
  </div>
</template>

<script>
import Animation from './components/Animation';
import QuadToCircle from './components/Circle';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Animation,
    QuadToCircle,
    Footer
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
