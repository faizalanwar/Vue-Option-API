<template>
    <table border="1" cellspacing="0" cellpadding="12">
        <tr>
            <th>Pengeluaran</th>
            <th>Keterangan</th>
        </tr>
        <tr v-for="(pengeluaran,index) in dataPengeluaran" v-bind:key="index">
            <td>{{pengeluaran.nominal}}</td>
            <td>{{pengeluaran.keterangan}}</td>
        </tr>
    </table>
</template>
<script>
export default {
    props:{
        dataPengeluaran: Array
    }
}
</script>

<style scoped>
table{
    border-collapse: collapse;
    width:100%
}
th{
    background-color: blueviolet;
    color: white;
}
tr:hover td{
    background-color: lightgrey;
    cursor: pointer;
}
</style>