<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImg @mudar-imagem="trocarImg" />
    </div>
</template>

<script>
import MudarImg from './MudarImg.vue';

export default {
    name: 'Picture',
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: "Zé_Henrique"
        };
    },
    components: { MudarImg },
    methods: {
        trocarImg() {
            this.avatar = "/img/avatar2.png"
        }
    }
}
</script>