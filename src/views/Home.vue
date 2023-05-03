<template>
  <VContainer>
    <VBtn @click="sanctum">Sanctum</VBtn>
  </VContainer>
</template>

<script setup>
  import axios from 'axios';
  axios.defaults.withCredentials = true;
  function sanctum() {
    axios.get('http://localhost:8000/sanctum/csrf-cookie').then(response => {
      // Login...
      console.log(response);
    });
  }
</script>
