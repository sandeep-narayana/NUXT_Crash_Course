<template>
    <div class="error-page">
      <p class="error-message">{{ error.message }}</p>
      <p class="error-status">{{ error.statusCode }}</p>
      <button class="go-home-button" v-on:click="HandelClearError()">Go to Home</button>
    </div>
  </template>
  
  <script setup>
  const { error } = defineProps(['error']);

  const HandelClearError =() => clearError({redirect:'/'})
  </script>
  
  <style scoped>
  .error-page {
    text-align: center;
    padding: 20px;
  }
  
  .error-message {
    font-size: 24px;
    color: red;
  }
  
  .error-status {
    font-size: 18px;
    color: darkred;
  }
  
  .go-home-button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
  }
  
  .hello-text {
    margin-top: 20px;
    font-size: 18px;
  }
  </style>
  