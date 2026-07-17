<template>
  <div class="app">
    <p>Username: {{ user.username }}</p>

    <p>
      <strong>Followers:</strong>
      {{ followers }}
    </p>

    <button type="button" @click="followUser">
      Follow User
    </button>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      followers: 0,

      user: {
        id: 1,
        username: "ChuaWL"
      }
    };
  },

  methods: {
    followUser() {
      this.followers += 1;
    }
  }
};
</script>

<style>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>