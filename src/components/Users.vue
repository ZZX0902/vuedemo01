<template>
  <div class="users">
    <h1>Hello Users</h1>
    <ul>
      <li v-for="item in users"
          v-on:click="item.show=!item.show">
        <h2>{{item.name}}</h2>
        <h2 v-show="item.show">{{item.position}}</h2>

      </li>
    </ul>
    <button v-on:click="deleteusers">删除</button>
  </div>

</template>
<!--
传值：string boolean number
引用：array object
 -->
<script>
  export default {
    name: "Users",
    props:["users"],
    // props: {
    //   users: {
    //     type: Array,
    //     request: true
    //   }
    // },
    data() {
      return {}
    },
    methods:{
      deleteusers:function () {
        this.users.pop();
      }
    }
  }
</script>

<style scoped>
  h1 {
    color: green;
  }

  .users {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;

  }

  ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
  }

  li {
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
  }
</style>
