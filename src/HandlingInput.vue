<template>
    <h1>Deret Bilangan Ganjil</h1>
    <h4>Bilangan {{bil}}</h4>
    <button v-on:Click="next">Next</button>

</template>

<script>
export default {
    data() {
        return{
            bil:1
        }
    },
    methods:{
     next(){
         this.bil += 1 ;
     }   
    }
}
</script>

<style scoped>

</style>