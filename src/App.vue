<script setup>


import MyInput from './components/MyInput.vue'

import { ref } from 'vue'
import MyInputs from './components/MyInputs.vue';
import MyListOfMyInputs from './components/MyListOfMyInputs.vue';

const text = ref('')

const listOfInputs = ref([[]])
</script>

<template>
  <MyListOfMyInputs v-model="listOfInputs" />
</template>

<style scoped>

</style>
