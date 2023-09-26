<template>
    <div>

        <button @click="primeiro(txt1,$event), segundo(txt2,$event),terceiro()">ativar múltiplos eventos</button>
        <p>{{ eventos }}</p>

    </div>
</template>

<script>
export default {
    name: 'MultiplosEventos',
    data() {
        return {
            eventos: "",
            txt1:"Primeiro evento",
            txt2:"Segundo evento"
        }
    },
    methods: {
        primeiro(txt,e) {
            this.eventos = txt
        },
        segundo(txt,e) {
            setTimeout(() => this.eventos = txt,500)
        },
        terceiro(){
            setTimeout(() => this.eventos = "último evento",2500)
        }
    }
}

</script>
<style scoped>
div {
    margin: 100px;
}
</style>