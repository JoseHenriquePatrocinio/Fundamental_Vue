<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Eu me chamo {{ nome }} e sou {{ profissao }}</p>
    <Info />
  </div>
</template>

<script>
import Info from "./Info.vue";
export default {
  name: `PrimeiroComponente`,
  components: {
    Info,
  },
  data() {
    return {
      nome: "José",
      profissao: "Desenvolvedor",
    };
  },
};
</script>