<template>
  <div class="home">
    <h1>Welcome to the App!</h1>
    <div>
      <p v-if="!loggedIn">
        To use this app you'll need to
        <router-link to="/login">Login</router-link> or
        <router-link to="/register">Register</router-link>
      </p>
    </div>
  </div>
</template>

<script>
import { authComputed } from '../vuex/helpers'
export default {
  computed: {
    ...authComputed
  }
}
</script>
