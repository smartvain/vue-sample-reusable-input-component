<template>
  <div>
    <BaseInput
      v-model:modalValue="userInputName"
      type="text"
      label="name"
    />
    <BaseInput
      v-model:modalValue="userInputEmail"
      type="email"
      label="email"
    />
    <BaseInput
      v-model:modalValue="userInputPassword"
      type="password"
      label="password"
    />
  </div>
</template>

<script setup lang="ts">
import BaseInput from './components/BaseInput.vue'
import { ref } from "vue"

const userInputName     = ref("")
const userInputEmail    = ref("")
const userInputPassword = ref("")
</script>

<style scoped>
</style>
