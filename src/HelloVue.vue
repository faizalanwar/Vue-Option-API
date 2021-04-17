<template>
  <h1>Hello Word</h1>
  <p>Projek Vue {{ nama }}</p>
  <p>Projek Vue {{ umur }}</p>
</template>

<script>
export default {
  data() {
    return {
      nama: "zal",
      umur: 12,
    }; 
  },
  mounted() {
    this.umur = this.umur + 3;
  },
};
</script>


<style scoped>
</style>