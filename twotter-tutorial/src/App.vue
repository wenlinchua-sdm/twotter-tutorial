//HTML
<template>
  <div id="app">
    {{user.username}}

    <strong> Followers : </strong> {{followers}}

    <button @click="followUser">
        Follow
    </button>

  </div>
</template>

//Java
<script>

export default {
  name: 'App',
  data() {
      return{
        followers : 0,
        user : {
            id: 1,
            username : 'ChuaWL',
        }
      }
  },

  method : {
    followUser(){
        this.followers++
    }
  }

}
</script>

//CSS
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
