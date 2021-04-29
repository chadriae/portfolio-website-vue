<template>

  <div id="container">

    <div id="tooltip" class="relative mx-2 mb-2">
      <div class="text-xs rounded py-1 px-4 right-0 bottom-full" :class="(mode === 'dark') ? 'background-white text-dark-transition' : 'background-dark text-white-transition'">
        Toogle {{ returnMode }} mode
        <svg class="absolute h-2 w-full left-0 top-full" :class="(mode === 'dark') ? 'text-white' : 'text-dark'" x="0px" y="0px" viewBox="0 0 255 255" xml:space="preserve"><polygon class="fill-current" points="0,0 127.5,127.5 255,0"/></svg>
      </div>
    </div>

    <Switch
      v-model="enabled"
      :class="enabled ? 'background-white' : 'background-dark'"
      class="focus:outline-none relative inline-flex items-center h-6 rounded-full w-11 border border-black"
      @click="$emit('toggle')"
    >
      <span
        :class="enabled ? 'transition duration-700 translate-x-1 button-color border border-black' : 'transition duration-700 translate-x-6 button-color border border-black'"
        class="focus:outline-none inline-block w-4 h-4 transform rounded-full"
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


<style scoped lang="scss">
@import "../styles/_variables.scss";

  .button-color {
    background-color: $button-color;
  }

  .background-dark {
    background-color: $dark-bg-color;
    transition: $transition;
  }

  .background-white {
    background-color: $white-color;
    transition: $transition;
  }

  .text-dark-transition {
    color: $dark-font-color;
    transition: $font-color-transition;
  }

  .text-white-transition {
    color: $white-color;
    transition: $font-color-transition;
  }

  .text-dark {
    color: $dark-font-color;
  }

  .text-white {
    color: $white-color;
  }

  #tooltip {
    opacity: 0;
    transition: opacity 0.3s ease-out; 
  }

  #container:hover #tooltip{
    opacity: 1;
    transition: $opacity-transition;
  }
</style>