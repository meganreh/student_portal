<template>
  <div class="container">
    <h1>Edit Info</h1>

    First Name:
    <input type="text" v-model="user.first_name" />
    <br />
    Last Name:
    <input type="text" v-model="user.last_name" />
    <br />
    Email:
    <input type="text" v-model="user.email" />
    <br />

    Password:
    <input type="text" v-model="user.password" />
    <br />

    Phone Number:
    <input type="text" v-model="user.phone_number" />
    <br />
    LinkedIn:
    <input type="text" v-model="user.linkedin" />
    <br />
    Twitter:
    <input type="text" v-model="user.twitter" />
    <br />
    Website:
    <input type="text" v-model="user.website" />
    <br />
    Resume:
    <input type="text" v-model="user.resume" />
    <br />
    Github:
    <input type="text" v-model="user.github" />
    <br />
    Photo:
    <input type="text" v-model="user.photo" />

    <br />
    Bio:
    <textarea cols="50" rows="10" type="text" v-model="user.bio" />
    <br />
    <button v-on:click="updateInfo(user)">Submit</button>
  </div>
</template>

<style></style>

<script>
import axios from "axios";

export default {
  data: function() {
    return {
      user: {}
    };
  },

  created: function() {
    axios.get("/api/users/" + this.$route.params.id).then(response => {
      this.user = response.data;
    });
  },

  methods: {
    updateInfo: function(user) {
      var params = {
        first_name: user.first_name,
        last_name: user.last_name,
        email: user.email,
        phone_number: user.phone_number,
        bio: user.bio,
        linkedin: user.linkedin,
        twitter: user.twitter,
        website: user.website,
        resume: user.resume,
        github: user.github,
        photo: user.photo
      };
      axios.patch("api/users/" + user.id, params).then(response => {
        this.$router.push("/");
      });
    }
  }
};
</script>
