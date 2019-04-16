<template>
  <div id="home">
    <Header v-on:titlechange="updatetitle($event)" v-bind:title="title"></Header>
    <p>传值更改只会更改其中一个，传引用更改会全部更改</p>
    <Users v-bind:users="users"> </Users>
    <Footer v-bind:title="title"></Footer>
  </div>
</template>

<script>
  import Header from './Header'
  import Footer from './Footer'
  import Users from './Users'


  export default {
    name: 'home',
    data(){
      return{
        users:[
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},
          {name:"lucy",position:"web 开发",show:false},


        ],
        title:"传递的是一个值，（number，string，boolean）"
      }
    },
    methods:{
      updatetitle(string){
        this.title=string;
      }


    },
    components: {
      "Header": Header,
      "Users": Users,
      "Footer": Footer

    },
    // created(){
    //   this.$http.get("http://jsonplaceholder.typicode.com/users")
    //     .then((data) => {
    //    this.users=data.body;
    //     })
    //}
  }
</script>


<style scoped>
  h1{
    color: purple;
  }

</style>

