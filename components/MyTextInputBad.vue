<script setup lang="ts">
const props = defineProps<{
  disabled?: boolean
}>()
</script>

<template>
  <FormKit type="text" :disabled="disabled">
    <template #label>CUSTOM LABEL</template>
  </FormKit>
</template>
