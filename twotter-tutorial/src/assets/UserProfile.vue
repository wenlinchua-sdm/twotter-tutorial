<template>
  <div class="user-profile">
    <div class="user-profile_user-panel">
      <h1 class="user-profile_username"> @{{user.username}} </h1>
      <div class="user-profile_followerCount">
        <strong> Followers : </strong> {{followers}}
      </div>
      <div class="user-profile_AdminBadge">
        admin
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserProfile",
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: "ChuaWL",
        isAdmin: false
      }
    };
  },

  watch : {
    followers(newFollowerCount, oldFollowerCount) {
      if(oldFollowerCount < newFollowerCount) {
        console.log(this.user.username + "has gain new followers");
      }
    }
  },

  methods: {
    followUser() {
      this.followers += 1;
    }
  },

  mounted() { //Keep the change
    this.followUser() ; //for example, follower count +1, even after refresh, it will not reset to 0
  }
};
</script>

<style>
.user-profile {
  display: grid;
  grid-template-columns: 1fr 3fr;
  width: 100%;
  padding: 50px 5%;
}

.user-profile_user-panel {
  display: flex;
  flex-direction: column;
  margin-right: 50px;
  padding: 20px;
  background-color: lightgray;
  border-radius: 10px;
  border: 1px solid black;
}
.user-profile_AdminBadge {
  background-color: azure;
  color: black;
  border-radius: 5px;
  margin-right: auto;
  padding: 0 10px;
}
</style>