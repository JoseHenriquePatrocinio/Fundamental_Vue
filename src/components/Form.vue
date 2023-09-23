<template>
  <div>
    <h2>Meu Formulário</h2>
    <form action="">
      <div>
        <InputText v-model="dinamico" />
      </div>
      <div>
        <InputText v-model="dinamico" />
      </div>
      <div>
        <Submit />
      </div>
    </form>
    <p>Você escreveu: {{ dinamico }}</p>
  </div>
</template>

<script>
import InputText from "./form/InputText.vue";
import Submit from "./form/Submit.vue";

export default {
  name: 'Form',
  components: {
    InputText,
    Submit,
  },

  data() {
    return {
      dinamico: "",
    }
  },
  methods: {

  }
};
</script>