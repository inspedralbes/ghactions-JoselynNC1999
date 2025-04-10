<template>
    <div class="teclat">
      <button v-for="n in 9" :key="n" @click="clicat(n)">
        {{ n }}
      </button>
      <p v-if="numero !== null">Has clicat el número: {{ numero }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  const numero = ref(null)
  const clicat = (n) => {
    numero.value = n
  }
  </script>
  
  <style>
  .teclat {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  .teclat button {
    width: 50px;
    height: 50px;
    font-size: 20px;
  }
  </style>
  