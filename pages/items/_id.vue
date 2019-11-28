<template>
  <div class="item">
    <h2>itemId: {{ id }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id
    }
  }
}
</script>
