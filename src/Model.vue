<template>
    <h1>Penggunaan Vmodel</h1>
    <h4>{{message}}</h4>
    <input type="text" v-model="message">
</template>

<script>
export default {
    data() {
       return{
           message:""
       } 
    },
}
</script>

<style scoped>

</style>