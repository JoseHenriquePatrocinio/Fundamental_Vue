<template>
    <div>
        <button @click="$emit('MudarImagem')">trocar img do perfil</button>
    </div>
</template>

<script>
export default{
    name:'MudarImg',
    emits:['MudarImagem']
}
</script>