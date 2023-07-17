<script lang="ts" setup>

defineProps({
  type: {type: String, required: true},
  label: {type: String, required: true},
  bgColor: {
    type: String, required: false, default: "bg-blue-500 text-white hover:bg-blue-600 focus:outline-\n" +
        "      none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 transition-all text-sm\n" +
        "      dark:focus:ring-offset-gray-800"
  },
  rounded: {type: Boolean, required: false, default: false}

})
</script>

<template>
  <button
      :class="[bgColor, rounded ? 'rounded-full' : '']"
      class="py-3 px-4 inline-flex justify-center items-center gap-2 rounded-md border
      border-transparent font-semibold ">
    {{ label }}
    <slot/>
  </button>
</template>

<style scoped>

</style>