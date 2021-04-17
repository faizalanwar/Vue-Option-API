<template>
  <form class="form-pengeluaran" @submit.prevent="catat">
    <div>
      <label for="">Pengeluaran</label>
      <input type="number" v-model="pengeluaran" id="pengeluaran"  />
    </div>
    <div>
      <label for="">Keterangan</label>
      <input type="text" v-model="keterangan" id="keterangan"  />
    </div>
    <div>
      <button>Catat</button>
    </div>
  </form>
</template>
<script>
export default {
  data() {
      return{
          pengeluaran: null,
          keterangan :null
      }
  },
  methods:{
      catat(){
          this.$emit('entri-pengeluaran',{
              nominal:this.pengeluaran,
              keterangan:this.keterangan,

          });
          this.pengeluaran = null;
          this.keterangan = null;
          document.getElementById("pengeluaran").focus();
      }
  }
};
</script>


<style scoped>
    .form-pengeluaran{
        padding:"20px";
        display:flex;
        flex-flow: row wrap;
        padding: 10px;
        margin: 5px 10px 5px 10px
    }
    
</style>