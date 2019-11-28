<template>
  <div class="item">
    <h2>Item detail</h2>
    <ul>
      <li>itemId: {{ item.id }}</li>
      <li>name: {{ item.name }}</li>
      <li>desc: {{ item.desc }}</li>
      <li>amount: {{ item.amount }}</li>
      <li>min: {{ item.min }}</li>
      <li>max: {{ item.max }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      item: {
        id: this.$route.params.id,
        name: 'hoge',
        desc: 'description',
        amount: 100,
        min: 10,
        max: 1000
      }
    }
  }
}
</script>
