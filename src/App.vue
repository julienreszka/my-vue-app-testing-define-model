<script setup>



import { ref } from 'vue'
import MyListOfMyInputs from './components/MyListOfMyInputs.vue';

const text = ref('')

const listOfInputs = ref([[]])
</script>

<template>
  <MyListOfMyInputs v-model="listOfInputs" />
</template>

<style scoped>

</style>
