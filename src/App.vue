<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      |

      <router-link to="/login" v-if="!jwt">Login!</router-link>

      |
      <router-link to="/logout" v-if="jwt">Logout</router-link>
    </div>
    <router-view v-on:theJwtChanged="updateJwt()" />
  </div>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  font-size: 30px;
  font-family: sans-serif;
}

#nav a {
  font-weight: bold;
  color: Navy;
  background-color: #4caf50; /* Green */
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
export default {
  data: function() {
    return {
      jwt: null
    };
  },
  created: function() {
    this.jwt = localStorage.jwt;
  },
  methods: function() {
    this.jwt = localStorage.jwt;
  }
};
</script>
