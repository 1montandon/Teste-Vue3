<script>
export default {
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
      if (this.contador > 0) 
      this.contador--
    },
    resetarContador() { 
      this.contador = 0
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
</script>

<template>
  <div class="container">
    <div></div>
    <div class="contador">
      <button @click="incrementarContador">Incrementar</button>
      <button @click="decrementarContador">Decrementar</button>
      <p>Valor do contador é: {{ contador }}</p>
      <button @click="resetarContador">Resetar</button>
    </div>
  </div>
</template>

<style scoped>
button{
  height: 50px;
  border: 1px 1px black;
  outline:none; 
  color: rgb(0, 0, 0);
  background-color: rgb(255, 255, 255);
  border-radius: 0%;
  transition: 0.5s;


}
button:hover{
  border-radius: 25%;
}
.container {
  display: grid;
  grid-template-rows: 2fr 1fr;
  justify-items: center;}
.contador{
  display: grid;
}
</style>
