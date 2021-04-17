<template>
    <h1>Loops</h1>
    <ol>
        <li v-for="hari in namaHari" v-bind:key="hari">{{hari}}</li>
    </ol>

    <table border="1" cellspacing="0" cellpadding="10">
        <tr>
            <td  v-for="hari in namaHari" v-bind:key="hari" >{{hari}}</td>
        </tr>
    </table>
</template>
<script>
export default {
    data() {
        return{
            namaHari:["senin","selasa","rabu","kamis","jumat","sabtu","minggu"]
        }
    }, 
}
</script>
<style scoped>

</style>