<template>
  <div class="app" :class="(mode === 'dark') ? 'dark-bg' : ''">
    <div class="mx-4 lg:m-auto content">
      <div class="flex justify-between sm:relative">
        <Hello :mode="mode" />
        <div class="sm:absolute sm:top-0 sm:right-0">
          <Switch @toggle="toggle" :mode="mode" />
        </div>
      </div>
      <About :mode="mode" />
      <Projects :mode="mode" />
      <!-- <Articles /> -->
      <Contact :mode="mode" />
    </div>
  </div>
</template>

<script>
import Switch from './tools/Switch'
import Hello from './components/Hello.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
// import Articles from './components/Articles.vue'
import Contact from './components/Contact.vue'


export default {
  name: 'App',
  data() {
    return {
      mode: 'light'
    }
  },
  components: {
    Switch,
    Hello,
    About,
    Projects,
    // Articles,
    Contact
  },
  methods: {
    toggle () {
      if (this.mode === 'dark') {
        this.mode = 'light'
      }
      else {
        this.mode = 'dark'
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import "./styles/_variables.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.content {
  padding: 50px 0 50px 0;
  max-width: 62rem;
  font-family: $font-family;
  text-align: center;
  margin: auto; 
  min-height: 100vh;
}

.app {
  background-color: $white-color;
  transition: $transition;
}

.dark-bg {
  background-color: $dark-bg-color;
  transition: $transition
}

@media (max-width: 400px){
  #app{
    /* width: auto; */
    margin: auto;
  }
}
</style>
