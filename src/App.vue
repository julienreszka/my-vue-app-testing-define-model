<script setup>
import { ref } from "vue";
import MyListOfMyInputs from "./components/MyListOfMyInputs.vue";

const listOfInputs = ref([[]]);
</script>

<template>
  <div class="d-flex gap">
    <div> 
      <pre>
      listOfInputs: {{ listOfInputs }}
    </pre
      >
    </div>
    <div>
      <MyListOfMyInputs v-model="listOfInputs" />
    </div>
  </div>
</template>

<style scoped></style>
