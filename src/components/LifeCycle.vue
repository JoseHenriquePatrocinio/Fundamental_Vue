<template>
  <h1>meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
  name: `LifeCycle`,
  data() {
    return {
      nome: `Deixa eu lembrar...`,
    };
  },
  created() {
    setTimeout(() => {
        this.nome = "José...alguma coisa"
    }, 3000);
    this.LifeCycle();
  },
  mounted(){
    setTimeout(() => {
        this.nome = "José Patrocinio"
    }, 6000);
    this.LifeCycle();
  },
  methods:{
    LifeCycle(){
      console.log("Execute");
    }
  }
};
</script>