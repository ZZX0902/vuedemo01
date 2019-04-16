<template>
  <div id="app">
    <li><router-link to="/home">home</router-link></li>
    <li><router-link to="/HelloWord">hello</router-link></li>
    <router-view></router-view>
  </div>
</template>

<script>



  export default {
    name: 'App',
    data(){
      return{

      }
    },
    methods:{


    },

  }
</script>


<style scoped>


</style>

