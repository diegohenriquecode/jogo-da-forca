<template>
  <div class="teclado">
    <button
      class="teclado-botao"
      v-for="(letra,
      key) in 'abcdefghijklmnopqrstuvwxyz0123456789!@#$%¨&*()_-.,'"
      :key="key"
      :disabled="verificarLetra(letra)"
      v-on:click="jogar(letra)"
    >
      {{ letra }}
    </button>
  </div>
</template>

<script>
export default {
  name: "Teclado",
  props: {
    letras: String,
    verificarLetra: Function,
    jogar: Function,
  },
  data() {
    return {};
  },
  methods: {},
  components: {},
};
</script>

<style>
.teclado {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 85%;
  margin-top: 20px;
}

.teclado-botao {
  margin: 5px;
  text-transform: uppercase;
}
</style>
