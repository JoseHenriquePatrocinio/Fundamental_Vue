<template>
  <div>
    <h2>Meu Formulário</h2>
    <form action="" @submit="enviarForm($event)">
      <div>
        <input type="text" v-model="name">
      </div>
      <div>
        <input type="text" v-model="email">
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
      name: "",
      email: ""
    }
  },
  methods: {
    enviarForm(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      alert("Form Enviado");
      console.log("Nome: " + name);
      console.log("Email: " + email)

      //realizar ação CRUD
    }
  }
};
</script>