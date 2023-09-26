<template>
  <div>
    <h1>Olá Vue!</h1>
    <Reutilizacao />
    <p>Eu me chamo {{ nome }} e sou {{ profissao }}</p>
    <Info />
    <Reutilizacao />
    <MultiplosEventos />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue";
import Reutilizacao from "./Reutilizacao.vue";
import Info from "./Info.vue";
export default {
  name: `PrimeiroComponente`,
  components: {
    Info,
    MultiplosEventos,
    Reutilizacao
  },
  data() {
    return {
      nome: "José",
      profissao: "Desenvolvedor",
    };
  },
};
</script>