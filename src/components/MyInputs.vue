<template>

  <div
    v-for="(item, itemI) in modelValue"
    :key="itemI"
  >
    <MyInput v-model="modelValue[itemI]" />
    <button @click="modelValue[itemI]=''">
      Clear
    </button>
  </div>
  <MyInput v-model="newItem" 
    label="Add new item"
    @keyup.enter="addNewItem()"
  />
  <button
    @click="addNewItem()"
  >
    Add to list
  </button>

</template>

<script setup lang="ts">
import { ref } from 'vue';
import MyInput from './MyInput.vue';

const modelValue = defineModel<string[]>()
const newItem = ref('')

const addNewItem = ()=>{
  console.log('addNewItem')
  modelValue.value = [...modelValue.value, newItem.value]
  newItem.value = ''
  console.log(modelValue.value)
}


</script>
