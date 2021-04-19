<template>
  <Hello />
  <About />
  <Projects />
</template>

<script>
import Hello from './components/Hello.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    Hello,
    About,
    Projects
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 1000px;
  text-align: center;
  margin: auto;
}
</style>
