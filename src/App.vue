<template>
  <HelloWorld msg="Hello  Faizal Anwar"/>
  <Title title="Catatan pengeluaran"/>
  <h4>Total Pengeluaran : {{totalPengeluaran}}</h4>
  <p v-if="warning">Warnning woiii</p>
  <formPengeluaran @entri-pengeluaran="entriPengeluaran($event)"/>
  <listPengeluaran v-if="showList" :dataPengeluaran="dataPengeluaran"/>
</template> 

<script>
import HelloWorld from './components/HelloWorld.vue'
import Title from "./components/Title.vue";
import listPengeluaran from"./components/listPengeluaran.vue";
import formPengeluaran from "./components/formPengeluaran.vue"
export default {
  name: 'App',
  components: {
    HelloWorld, 
    Title,
    listPengeluaran,
    formPengeluaran
  },
  data(){
    return{
      dataPengeluaran:[
        {nominal:20000,keterangan:"makan siang"},
        {nominal:10000,keterangan:"bensin"},
        {nominal:15000,keterangan:"pulsa"}
      ],
      warning:false,
    }
  },
  methods:{
    entriPengeluaran(event){
      this.dataPengeluaran.push(event);
    }
  },
  computed:{
    showList:function(){
      return this.dataPengeluaran.length>0 ;
    },
    totalPengeluaran:function(){
      return this.dataPengeluaran.reduce((angka,item)=>angka+parseInt(item.nominal),0)
    }
  },
  watch:{
    totalPengeluaran:function(val){
      if(val>50000){
        this.warning=true;
      }
    }
  }  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
