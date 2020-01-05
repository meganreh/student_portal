<template>
  <div class="home">
    <h1>Info</h1>
    <div v-for="student in students">
      <h2>{{ student.first_name }}</h2>
    </div>
  </div>
</template>

<style></style>

<script>
export default {
  data: function() {
    return {
      message: "Student Portal Fun Time",
      students: [
        {
          id: 1,
          first_name: "Peter",
          last_name: "Name",
          email: "peter@email.com",
          password: "password",
          phone_number: "123456789",
          bio: "x",
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
