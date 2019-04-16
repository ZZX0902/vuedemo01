<template>
  <footer>
    <h2>{{copy}}{{title}}</h2>
  </footer>
</template>

<script>
  export default {
    name: "Footer",
    props:{
      title:{
        type:String
      }
    },
    data(){
      return{
        copy:"ZZX 2019 vue demo 01"
      }
    }
  }
</script>

<style scoped>
  footer{
    background: rgba(0, 0, 0, 0.98);
    padding: 6px;
  }
  h2{
    color: rgba(11, 135, 66, 0.99);
    text-align: center;
  }
</style>
