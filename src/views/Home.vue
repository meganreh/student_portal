<template>
  <div class="home">
    <h1>Info</h1>
    <div v-for="user in users">
      <h2>{{ user.first_name }} {{ user.last_name }}</h2>
      <h3>Email: {{ user.email }} | Phone: {{ user.phone_number }}</h3>
      <h4>Bio: {{ user.bio }}</h4>
      LinkedIn: {{ user.linkedin }} | Twitter: {{ user.twitter }} Website: {{ user.website }} | Resume:
      {{ user.phone_number }} Github: {{ user.github }} | Photo: {{ user.photo }}
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
      users: [{}]
    };
  },
  created: function() {
    axios.get("api/users").then(response => {
      this.users = response.data;
    });
  },
  methods: {}
};
</script>
