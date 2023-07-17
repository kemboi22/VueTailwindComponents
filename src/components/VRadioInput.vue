<script lang="ts" setup>
defineProps({
  label: {type: String, required: true},
})
</script>

<template>

  <div class="flex items-center">
    <input class="h-4 w-4 border-gray-300 text-indigo-600 focus:ring-indigo-600" type="radio">
    <label class="ml-3 block text-sm font-medium leading-6 text-gray-900">{{ label }}</label>
  </div>


</template>

<style scoped>

</style>