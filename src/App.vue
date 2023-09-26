<template>
  <div>

    <Header></Header>
    <a v-bind:href="link" target="_blank">Rick </a>
    <PrimeiroComponente />
    <p class="paragrafo_pai">{{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Pessoa from "./components/Pessoa.vue";

export default {
  name: `App`,
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header
  },
  data() {
    return {
      testando: "Teste",
      link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
    }
  }
};
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}

a {
  color: red;
}

.teste {
  background-color: black;
}
</style>