<script lang="ts" setup>
defineProps({
  label: {type: String, required: true},
  rounded: {type: Boolean, required: false, default: false},
  rows: {type: Number, required: false, default: 4},
})
</script>

<template>
  <div>
    <label class="block text-sm font-medium leading-6 text-gray-900 dark:text-white">{{ label }}</label>
    <div class="mt-2">
      <textarea
          :class="[rounded ? 'rounded-full' : '']"
          :rows="rows"
          class="block w-full rounded-md border-0 py-1.5 text-gray-900 dark:text-white shadow-sm ring-1 ring-inset
          ring-gray-300 placeholder:text-gray-400 dark:placeholder:text-white/5 focus:ring-2 focus:ring-inset focus:ring-indigo-600
           sm:text-sm sm:leading-6 dark:bg-slate-900 dark:border-gray-700"
      />
    </div>
  </div>
</template>

<style scoped>

</style>