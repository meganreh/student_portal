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
      message: "Student Portal Fun Time",
      user: {
        id: 1,
        first_name: "Peter",
        last_name: "Name",
        email: "peter@email.com",
        password: "password",
        phone_number: "123456789",
        bio: "He's a weird guy",
        linkedin: "x",
        twitter: "x",
        website: "x",
        resume: "x",
        github: "x",
        photo: "x"
      }
    };
  },

  created: function() {
    this.user = {
      id: 1,
      first_name: "Peter",
      last_name: "Name",
      email: "peter@email.com",
      password: "password",
      phone_number: "123456789",
      bio: "He's a weird guy",
      linkedin: "x",
      twitter: "x",
      website: "x",
      resume: "x",
      github: "x",
      photo: "x"
    };
  },

  methods: {}
};
</script>
