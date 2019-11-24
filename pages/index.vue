<template>
  <div class="container">
    <logo />
    <router-link class="navbar-brand" to="/about">About</router-link>
    <h1 class="title">
      prevent-loss
    </h1>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
