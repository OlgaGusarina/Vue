<template>
  <div class="block">
    <h1>Let's calculate!</h1>
    <div class="display">
      <input class="usernumber" v-model="operand1" />
      <input class="usernumber" v-model="operand2" />
      <div class="result">= {{ result }}</div>
    </div>
    <div class="keyboard">
      <button v-on:click="result = +operand1 + +operand2">+</button>
      <button v-on:click="result = operand1 - operand2">-</button>
      <button @click="result = Math.round((operand1 / operand2) * 100) / 100">
        / 0.00
      </button>
      <button @click="result = Math.round(operand1 / operand2)">/ 0</button>
      <button @click="result = operand1 * operand2">*</button>
      <button @click="result = Math.pow(operand1, operand2)">^</button>
    </div>
  </div>
</template>
 
<script>
export default {
  name: "Calculator",
  data() {
    return {
      operand1: 0,
      operand2: 0,
      result: 0,
    };
  },
};
</script>

<style>
button {
  background-color: cornsilk;
}
.block {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.display {
  display: flex;
  gap: 16px;
  align-self: center;
  width: 200px;
  height: 32px;
}
.usernumber {
  width: 20%;
  text-align: center;
}
.result {
  display: flex;
  align-items: center;
}
.keyboard {
  display: flex;
  justify-content: center;
  gap: 16px;
}
</style>
