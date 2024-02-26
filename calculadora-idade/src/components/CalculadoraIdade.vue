<!-- src/components/CalculadoraIdade.vue -->

<template>
  <div class="calculadora-idade">
    <label for="dataNascimento">Data de Nascimento:</label>
    <input type="date" id="dataNascimento" v-model="dataNascimento" />

    <button @click="calcularIdade">Calcular Idade</button>

    <div v-if="idade !== null">
      <p class="resultado">Sua idade é: {{ idade }} anos</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dataNascimento: null,
      idade: null,
    };
  },
  methods: {
    calcularIdade() {
      if (this.dataNascimento) {
        const hoje = new Date();
        const dataNascimento = new Date(this.dataNascimento);
        const diff = hoje - dataNascimento;
        const idade = Math.floor(diff / (1000 * 60 * 60 * 24 * 365.25));
        this.idade = idade;
      }
    },
  },
};
</script>

<style scoped>
.calculadora-idade {
  max-width: 400px;
  margin: 50px auto;
  padding: 20px;
  background-color: #9ee192;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 10px;
}

input {
  width: 100%;
  padding: 8px;
  margin-bottom: 15px;
  box-sizing: border-box;
  border: 1px solid #ddd;
  border-radius: 4px;
}

button {
  background-color: #007bff;
  color: #fff;
  padding: 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

.resultado {
  margin-top: 20px;
  font-weight: bold;
}

</style>
