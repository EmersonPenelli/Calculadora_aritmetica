<template>
  <div class="container mt-5">
    <div class="card">
      <div class="card-body">
        <h1 class="">Calculadora Aritmética</h1>
        <h3 class="text-start">
            - Para utilizar a calculadora, comece inserindo o primeiro valor
            numérico no campo indicado.
        </h3>
        <h3 class="text-start">
            - Em seguida, selecione a operação desejada: soma,
            subtração,multiplicação ou divisão à partir do menu suspenso.
        </h3>
        <h3 class="text-start">
            - Após escolher a operação, digite o segundo número no próximo
            campo. Assim que ambos os números e a operação estiverem definidos,
            acalculadora processará automaticamente e exibirá o resultado da
            operação escolhida.
        </h3>

        <div class="input-group mb-3">
          <input type="number" class="form-control" v-model.number="numero1" />
        </div>

        <div class="input-group mb-3">
          <select class="form-select" v-model="operacao">
            <option value="adicao">+</option>
            <option value="subtracao">-</option>
            <option value="multiplicacao">*</option>
            <option value="divisao">/</option>
          </select>
        </div>

        <div class="input-group mb-3">
          <input type="number" class="form-control" v-model.number="numero2" />
        </div>

        <p class="mt-3 fs-2">Resultado: {{ resultado }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: "adicao",
    };
  },
  computed: {
    resultado() {
      switch (this.operacao) {
        case "adicao":
          return this.numero1 + this.numero2;
        case "subtracao":
          return this.numero1 - this.numero2;
        case "multiplicacao":
          return this.numero1 * this.numero2;
        case "divisao":
          return this.numero2 !== 0
            ? this.numero1 / this.numero2
            : "Divisão por zero";
        default:
          return 0;
      }
    },
  },
};
</script>
