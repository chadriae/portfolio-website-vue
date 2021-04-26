<template>

  <div id="container">

    <div id="tooltip" class="relative mx-2 mb-2">
      <div class="bg-black text-white text-xs rounded py-1 px-4 right-0 bottom-full">
        Toogle {{ returnMode }} mode
        <svg class="absolute text-black h-2 w-full left-0 top-full" x="0px" y="0px" viewBox="0 0 255 255" xml:space="preserve"><polygon class="fill-current" points="0,0 127.5,127.5 255,0"/></svg>
      </div>
    </div>

    <Switch
      v-model="enabled"
      :class="enabled ? 'background-white' : 'background-dark'"
      class="relative inline-flex items-center h-6 rounded-full w-11 border border-black"
      @click="$emit('toggle')"
    >
      <span
        :class="enabled ? 'transition duration-700 translate-x-1 bg-yellow-500' : 'transition duration-700 translate-x-6 bg-yellow-200'"
        class="inline-block w-4 h-4 transform rounded-full"
      />
    </Switch>

  </div>

</template>

<script>
  import { ref } from "vue";
  import { Switch } from "@headlessui/vue";

  export default {
    props: ['mode'],
    emits: ['toggle'],
    components: { 
      Switch,
    },
    setup() {
      const enabled = ref(false);
      return { 
        enabled,
      };
    },
    computed: {
      returnMode() {
        if (this.mode == 'dark') {
          return 'light';
        } else {
          return 'dark';
        }
      }
    },
  }

</script>


<style scoped>
  .background-dark {
    background-color: #1E2228;
    transition: background 0.7s ease-in-out;
  }

  .background-white {
    background-color: white;
    transition: background 0.7s ease-in-out;
  }

  #tooltip {
    opacity: 0;
    transition: opacity 0.5s ease-out;
  }

  #container:hover #tooltip{
    opacity: 1;
    transition: opacity 0.5s ease-out;
  }
</style>