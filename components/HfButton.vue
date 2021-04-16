<template>
  <Button
    class="bg-blue-500 hover:bg-blue-700 text-white text-lg font-bold py-2 px-4 rounded"
  >
    {{ label }}
  </Button>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    label: {
      type: String,
      default: 'Button',
    },
  },
})
</script>