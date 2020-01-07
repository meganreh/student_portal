<template>
  <div class="home">
    <h1>Info</h1>
    <div v-for="user in users">
      <h2>{{ user.first_name }} {{ user.last_name }}</h2>
      Email: {{ user.email }} | Phone: {{ user.phone_number }}
      <br />
      Bio: {{ user.bio }}
      <router-link v-bind:to="`/user/${user.id}`">Edit</router-link>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";
export default {
  data: function() {
    return {
      message: "Student Portal Fun Time",
      users: [
        {
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
      ]
    };
  },

  created: function() {},

  methods: {}
};
</script>
