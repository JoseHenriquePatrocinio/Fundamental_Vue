<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para backend:</p>
    <ul>
      <li v-for="(technology, index) in backendTech" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo as seguintes tecnologias para frontend:</p>
    <ul>
      <li v-for="technology in frontendTech" v-bind:key="technology.id">{{ technology.lang }}</li>
    </ul>
    <div>
      <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui </a></p>
    <Picture></Picture>
  </div>
</template>

<script>
import Picture from './Picture.vue';
export default {
  name: `Info`,
  components: {
    Picture
  },
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: "henriquepatrocinio98@gmail.com",
      meu_link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
      textoBotao:"Mostrar e-mail",
      backendTech: ['Javascript','Python','C#','C++'],
      frontendTech:[{id:1,lang:'Vue'},{id:2,lang:'HTML'},{id:3,lang:'CSS'}]
    }
  },
  methods:{
    showEmail(){
      this.mostrar_email = !this.mostrar_email
      if(!this.mostrar_email){
        this.textoBotao = "Mostrar e-mail"
      }else{
        this.textoBotao = "Esconder e-mail"
      }
    }
  }
};
</script>

<style>
.paragrafo_pai{
  color: aquamarine;
}
</style>