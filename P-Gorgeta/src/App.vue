<script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>
<template>
  <div class="inputs">
    <input type="text" v-model="valor1" placeholder="Valor da conta" />

    <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
      <option value="5">5% (Péssimo)</option>
      <option value="10">10% (n lembro)</option>
      <option value="15">15% ()</option>
      <option value="20">20% ()</option>
      <option value="25">25% ()</option>
    </select>

    <input type="text" placeholder="Quantidade de amigos" v-model="valor2" />

    <p>
      Valor para cada um pagar: R$ {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}
    </p>
  </div>
</template>

<style>
.inputs {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid bl;
  padding: 10px;
  background-color: lightblue;
}

input {
  margin: 10px;
}

p {
  border: 1px solid black;
  padding: 2px;
  background-color: white;
}
body {
  background: linear-gradient(gray, white);
}
</style>
