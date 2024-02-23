<script setup>
import{ ref } from 'vue' //importando uma fnção do vue chamada "ref"

const contador = ref(0)  // ref define um numero a uma variavel

function incrementarContador() {
  contador.value++
}

function decrementarContador() {
  if (contador.value > 0) // contador.value > 0, permite que o contador não fique negativo
  contador.value--
}

function redefinir(){
  contador.value = 0
}

console.log(`o valor do contador é: `)

/*export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      this.contador--
    },
    redefinir(){
      contador.value = 0
    }
  },
  onMounted() => {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
*/

</script>

<template>
  <p>o valor do contador é : {{ contador }}</p>

  <div class="buttons">
    <button @click="incrementarContador">+</button>
    <button @click="decrementarContador">-</button>
    <button @click="redefinir">redefinir</button>
  </div>
</template>

<style scoped>

*{
  display: flex;
  justify-content: center;
}

.buttons{
  text-align: center;
}
</style>
