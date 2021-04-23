<template>
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
  
</template>

<script>
  import { ref } from "vue";
  import { Switch } from "@headlessui/vue";

  export default {
    props: ['mode'],
    emits: ['toggle'],
    components: { Switch },
    setup() {
      const enabled = ref(false);
      return { enabled };
    },
  };

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

</style>