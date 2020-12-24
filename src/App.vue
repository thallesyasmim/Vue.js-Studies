<template>
  <div id="app">
    <h1>{{ vuejs }}</h1> <!-- Interpolation -->
    <!-- {{ 341 + 86 - 62 }}  JavaScript Expressions -->
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
  },
  data() { // Component Data
    return { 
      vuejs: 'Vue.js: Reactive Framework'
    }
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
