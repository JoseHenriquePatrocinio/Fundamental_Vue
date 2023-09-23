<template>
  <input type="text" v-model="inputValue" />
</template>

<script>
export default {
  name: 'InputText',
  data() {
    return {
      inputValue: ''
    }
  }
}
</script>