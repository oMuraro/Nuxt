<template>
  <div>
    <input v-model="inputDados" type="text" name="" id="">
    <button @click = "receberDados">Adicionar</button>
    <ul>
      <li v-for="n in nome"> {{ n }} </li>
    </ul>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        nome: [],
        inputDados: ""
      }
    },
    methods: {
      receberDados() {
        this.nome.push(this.inputDados)
      }
    }
  }
</script>