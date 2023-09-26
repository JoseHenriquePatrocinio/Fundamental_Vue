<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Eu me chamo {{ nome }} e sou {{ profissao }}</p>
    <Info />
    <MultiplosEventos />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue";
import Info from "./Info.vue";
export default {
  name: `PrimeiroComponente`,
  components: {
    Info,
    MultiplosEventos
  },
  data() {
    return {
      nome: "José",
      profissao: "Desenvolvedor",
    };
  },
};
</script>