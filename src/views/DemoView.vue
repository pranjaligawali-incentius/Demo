<script setup>
import { ref, reactive } from 'vue' // Added quotes around 'vue'

const myObject = reactive({
  title: 'How to do lists in Vue', 
  author: 'Jane Doe',             
  publishedAt: '2026-3-12'        
})
</script>

<template>
  <header>
    <ul>
      <!-- Added quotes around the expression -->
      <li v-for="(value, key) in myObject" :key="key">
        {{ key }}: {{ value }}
      </li>
    </ul>
  </header>
</template>
