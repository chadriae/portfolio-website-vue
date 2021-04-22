<template>
  <Switch
    v-model="enabled"
    :class="enabled ? 'bg-gray-800' : 'bg-white'"
    class="relative inline-flex items-center h-6 rounded-full w-11 border border-black sun"
    @click="$emit('toggle')"
  >
    <span
      :class="enabled ? 'transition duration-700 translate-x-6 bg-yellow-200' : 'transition duration-700 translate-x-1 bg-yellow-500'"
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
</style>