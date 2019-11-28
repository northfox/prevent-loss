<template>
  <div class="wrap">
    <Header></Header>
    <main>
      <nuxt />
    </main>
    <Footer></Footer>
  </div>
</template>

<style>
body,
.wrap {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  margin: 0px;
  padding: 0px;
}

footer {
  margin-top: auto;
}
</style>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>
