<template>
  <div class="container">
    <logo />
    <router-link class="nav-link" to="/about">About</router-link>
    <router-link class="nav-link" to="/references">References</router-link>
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
