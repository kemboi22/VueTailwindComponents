<script lang="ts" setup>
import {ExclamationCircleIcon} from '@heroicons/vue/20/solid'

defineProps({
  label: {type: String, required: true},
  type: {type: String, required: true},
  placeholder: {type: String, required: false, default: ""},
  rounded: {type: Boolean, required: false, default: false},
  error: {type: String, required: false, default: ""},
  success: {type: String, required: false, default: ""},


})
</script>

<template>
  <div>
    <label class="block text-sm font-medium leading-6 text-gray-900 dark:text-white">{{ label }}</label>
    <div class="mt-2 relative">
      <input :class="[rounded ? 'rounded-full' : '']"
             :placeholder="placeholder"
             :type="type"
             class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2
             focus:ring-inset  focus:ring-indigo-600 sm:text-sm sm:leading-6 dark:bg-slate-900 dark:border-gray-700 dark:text-gray-400"
      />
      <div v-if="error !== ''" class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-3">
        <ExclamationCircleIcon class="h-5 w-5 text-red-500"/>
      </div>
    </div>
    <p v-if="error !== ''" class="text-sm text-red-600 mt-2">{{ error }}</p>
    <p v-if="success !== ''" class="text-sm text-green-600 mt-2">{{ success }}</p>
  </div>
</template>

<style scoped>

</style>