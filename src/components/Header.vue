<template>
    <ul>
        <li> <a href="link">Home</a></li>
        <li> <a v-bind:href="link" target="_blank">Project</a></li>
        <li> <a href="link">Contact</a></li>
    </ul>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
        }
    }
}
</script>

<style scoped>
ul {
    list-style: none;
    display: flex;
}

li {
    margin-right: 10px;
}

a {
    color: burlywood;
    text-decoration: none;
    transition: .5s;
}

a:hover {
    color: turquoise;
}
</style>