<template>
  <div
    v-for="(item, itemI) in modelValue"
    :key="itemI"
  >
    <div>
      List {{ itemI  }}
    </div>
    <MyInputs v-model="modelValue[itemI]" />
  </div>

  <button
    @click="addAList()"
  >
    Add a list
  </button>
</template>

<script setup lang="ts">
import MyInputs from './MyInputs.vue';


const modelValue = defineModel<string[][]>()
const addAList = ()=>{
  console.log('addAList')
  modelValue.value = [...modelValue.value, []]
  console.log(modelValue.value)
}

</script>
