<script setup>
import { ref } from "vue";
import MyListOfMyInputs from "./components/MyListOfMyInputs.vue";


const listOfInputs = ref([[]]);
</script>

<template>
  <div>
    <pre>
      listOfInputs: {{ 
        listOfInputs
        }}
    </pre>
  </div>
  <div>
    <MyListOfMyInputs v-model="listOfInputs" />
  </div>
</template>

<style scoped></style>
