<script setup>
import{ ref } from 'vue'

const contador =ref(0)  

function incrementarContador() {
  contador.value++
}

function decrementarContador() {
  contador.value--  
}
</script>

<template>
  <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <p>o valor do contador é : {{ contador }}</p>
</template>

<style scoped>

</style>
