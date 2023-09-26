<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email" />
    <Form></Form>
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
  </div>
</template>

<script>
import Info from "./Info.vue";
import Form from "./Form.vue";
import Reutilizacao from "./Reutilizacao.vue";

export default {
  name: "Pessoa",
  components: {
    Info,
    Form,
    Reutilizacao
  },
  data() {
    return {
      nome: "Henrique",
      email:"zehenrique@gmail.com"
    };
  },
};
</script>
