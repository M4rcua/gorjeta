<script setup>
import { ref } from "vue";

const pessoas = ref("");
const valor = ref("");
const gorgeta = ref("");
</script>
<template>
  <div class="container">
    <h1>Calculadora para gorgetas</h1>
    <input type="text" v-model="valor" placeholder="Valor da conta" />

    <select name="Qualidade de serviço" id="" v-model="gorgeta">
      <option value="1" selected="selected">
        Escolha a qualidade do serviço
      </option>
      <option value="1.05">5% (Péssimo)</option>
      <option value="1.10">10% (Ruim)</option>
      <option value="1.15">15% (Ok)</option>
      <option value="1.20">20% (Bom)</option>
      <option value="1.25">25% (Muito bom)</option>
      <option value="1.30">30% (Excepcional)</option>
    </select>

    <input type="text" placeholder="Quantidade de pessoas" v-model="pessoas" />

    <p>
      Valor por pessoa: R$
      {{ Math.ceil(((valor * gorgeta) / pessoas) * 100) / 100 }}
    </p>
  </div>
</template>

<style>
.container {
  margin: 100px auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1px solid grey;
  border-radius: 12px;
  width: 390px;
  height: 450px;
  padding: 0px 15px 13px 13px;
  background-color: rgb(255, 196, 0);
}

input,
select,
p {
  margin: 20px;
  width: 280px;
  height: 30px;
}

p {
  border: 1px solid black;
  padding: 2px 6px;
  background-color: white;
}
body {
  background: linear-gradient(rgb(56, 56, 56) rgb(97, 97, 97));
  height: 665px;
}
</style>
