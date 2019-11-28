<template>
  <header class="header">
    <logo />
    <router-link class="nav-link" to="/about">About</router-link>
    <router-link class="nav-link" to="/references">References</router-link>
  </header>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
