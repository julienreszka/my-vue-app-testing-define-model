
<template>

<!-- <label>{{ label }}</label> -->
<input type="text" v-model="modelValue" />


</template>

<script setup lang="ts">
const modelValue = defineModel<string>()

defineProps({
  label: String,
})
</script>
