<template>
  <div id="app">
    <h1>{{ vuejs }}</h1> <!-- Interpolation -->
    <Input />
    <!-- {{ 341 + 86 - 62 }}  JavaScript Expressions -->
    <Animation /> 
    <QuadToCircle @alertCircles="emitAlert($event)" />
    <Footer :directive="directive" />
    <Footer :footer="footer" />
    <Footer />
  </div>
</template>

<script>
import Animation from './components/Animation';
import QuadToCircle from './components/Circle';
import Footer from './components/Footer';
import Input from './components/Input';

export default {
  name: 'App',
  components: {
    Animation,
    QuadToCircle,
    Footer,
    Input
  },
  data() { // Component Data
    return { 
      vuejs: 'Vue.js: Reactive Framework',
      directive: "The directive in Vue.js allowed me to appear",
      footer: {
        framework: 'Vue.js',
        author: 'Thalles Gabriel'
      }
    }
  },
  methods: {
    emitAlert($event) {
      const { circles } = $event.component
      const showFruits = $event.component.emitConfirm()
      if(showFruits) {
        const listFruits = circles.map(value => value.fruit)
        for (const fruit of listFruits) {
          alert(fruit)
        }
      }
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
