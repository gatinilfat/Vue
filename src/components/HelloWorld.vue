<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <hr>
    <div class="display">
      <input v-model.number="operand1" type="text">
      <input v-model.number="operand2" type="text">
      = {{ result }}
    </div>
    <div class="keyboard">
      <button @click="sum(operand1, operand2)">+</button>
      <button @click="minus(operand1, operand2)">-</button>
      <button @click="multi(operand1, operand2)">*</button>
      <button @click="divide(operand1, operand2)">/</button>
      <button @click="degree(operand1, operand2)">^</button>
      <button @click="intDivide(operand1, operand2)">intDivide</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    data() {
      return {
        operand1: 0,
        operand2: 0,
        result: 0,
      }
    },
    methods: {
      sum(op1, op2) {
        this.result = op1 + op2
      },
      minus(op1, op2) {
        this.result = op1 - op2
      },
      multi(op1, op2) {
        this.result = op1 * op2
      },
      divide(op1, op2) {
        this.result = op1 / op2
      },
      degree(op1, op2) {
        this.result = op1 ** op2
      },
      intDivide(op1, op2) {
        this.result = parseInt(op1 / op2)
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }

  button {
    padding: 5px 10px;
    background: none;
    margin: 5px;
    border:1px solid #35495e;
    border-radius: 5px;
  }
  button:hover {
    background: #41b883;
  }
</style>