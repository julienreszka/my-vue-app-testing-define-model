<template>
  <div
    v-for="(item, itemI) in modelValue"
    :key="itemI"
  >
    <div>
      List {{ itemI  }}
      <button
        @click="deleteList(itemI)"
      >
        Delete list
      </button>
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

const deleteList = (index: number)=>{
  console.log('deleteList')
  modelValue.value = modelValue.value.filter((_, i)=>i!==index)
  console.log(modelValue.value)
}

</script>
