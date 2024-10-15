<template>
  <button @click="login">login</button>
  <button @click="current_datetime">current_datetime</button>
</template>
<script setup>
import axios from 'axios'

let base_url = import.meta.env.VITE_APP_NGINX_URL

let token = null
axios.defaults.baseURL = base_url;
function login() {
  axios.post("/auth/login", {
    username: 'testuser',
    password: 'password123'
  }).then((data) => {
    token = data.data["token"]
  })
}
function current_datetime() {
  axios.get(base_url + '/api/current-datetime', {headers: {"Authorization": token}}).then((data) => {
    console.log(data.data)
  })
}
</script>
<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
