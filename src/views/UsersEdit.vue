<template>
  <div class="container">
    <h1>Edit Info</h1>
    First Name:
    <input type="text" v-model="user.first_name" />
    Last Name:
    <input type="text" v-model="user.last_name" />
    Email:
    <input type="text" v-model="user.email" />
    Phone Number:
    <input type="text" v-model="user.phone_number" />
    Bio:
    <input type="text" v-model="user.bio" />
    LinkedIn:
    <input type="text" v-model="user.linkedin" />
    Twitter:
    <input type="text" v-model="user.twitter" />
    Website:
    <input type="text" v-model="user.website" />
    Resume:
    <input type="text" v-model="user.resume" />
    Github:
    <input type="text" v-model="user.github" />
    Photo:
    <input type="text" v-model="user.photo" />
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
