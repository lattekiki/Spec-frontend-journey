<script setup>
import {ref} from 'vue'
const name = ref('')
</script>

<template>
  <input v-model="name" placeholder="Type your name...">
  <h1 v-if="name.length > 0"> Hi Everyone 👋, This is {{ name }}</h1>
  <p v-else> Please enter your name to see the greeting message.</p>
</template>
