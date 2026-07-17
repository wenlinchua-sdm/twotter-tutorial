<template>
  <div id ="app">
    <UserProfile/>
  </div>

</template>

<script>
import UserProfile from "./assets/UserProfile";

export default {
  name : 'app' ,
  components: { UserProfile }
}
</script>

<style>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>