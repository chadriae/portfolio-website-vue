<template>
  <div class="mx-8">
    <Hello />
    <About />
    <Projects />
    <!-- <Articles /> -->
    <Contact />
  </div>
</template>

<script>
import Hello from './components/Hello.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
// import Articles from './components/Articles.vue'
import Contact from './components/Contact.vue'


export default {
  name: 'App',
  components: {
    Hello,
    About,
    Projects,
    // Articles,
    Contact
  }
}
</script>

<style>
body {
    /* background-color: rgb(255, 255, 247); */
    /* background-color: #f9f9f1; */
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 62rem;
  text-align: center;
  margin: 2rem auto 2rem auto;
}

@media (max-width: 400px){
  #app{
    width: auto;
    margin: auto;
  }
}
</style>
