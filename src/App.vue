<script lang="ts" setup>

import VInput from "./components/VInput.vue";
import VButton from "./components/VButton.vue";
import VTextArea from "./components/VTextArea.vue";
</script>

<template>
  <VInput label="Email" rounded type="email"/>
  <VButton label="Button" rounded type="button">
    +
  </VButton>
  <VTextArea label="label"/>
</template>

<style scoped>

</style>
