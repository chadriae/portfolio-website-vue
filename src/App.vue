<template>
  <div class="mx-8">
    <Hello />
    <About />
    <Projects />
    <!-- <Articles /> -->
  </div>
</template>

<script>
import Hello from './components/Hello.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
// import Articles from './components/Articles.vue'


export default {
  name: 'App',
  components: {
    Hello,
    About,
    Projects,
    // Articles
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 62rem;
  text-align: center;
  margin: 7rem auto 7rem auto;
}
@media (max-width: 400px){
  #app{
    width: auto;
    margin: auto;
  }
}

</style>
