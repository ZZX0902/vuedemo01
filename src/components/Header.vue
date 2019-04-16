<template>
  <header v-on:click="titlechange">
    <h1>{{title1}}{{title}}</h1>
  </header>
</template>

<script>
  export default {
    name: "Header",
    props:{
      title:{
        type:String
      }
    },
    data(){
      return{
        title1:"Vue.js.demo"
      }
    },
    methods:{
      titlechange:function () {
        //this.title="changge"
        this.$emit("titlechange","子向父组件传值");
        //$emit 注册事件
      }
    },

    //beforeCreate:function () {
    // alert("组件实例化之前的函数");
    //},
    //created :function () {
    //  alert("组件实例化完毕 但页面还没显示");
    //},
   // beforeMount:function () {
    //  alert("组件挂载前，页面仍没展示，但虚拟Dom已经配置");
    //},
    //mounted:function () {
    //  alert("组件挂载后，此方法执行，页面显示");
    //},
    //beforeUpdate:function () {
    //  alert("组件更新前，页面仍没更新，但虚拟Dom已经配置");
    //},
    ///updated:function () {
    //alert("组件更新，页面显示");
    //},
    //beforeDestroy:function () {
    //  alert("组件销毁前");
    //},
    //destroyed:function () {
    //  alert("组件销毁");
    //}


  }

</script>


<style scoped>
  header{
    background: lightseagreen;
    padding: 10px;
  }
h1{
  color: aqua;
  text-align: center;
}
</style>
