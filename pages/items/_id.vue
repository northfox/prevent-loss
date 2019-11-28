<template>
  <div class="item">
    <h2>Item detail</h2>
    <button @click="isEditable = false" v-if="isEditable" type="button">save</button>
    <button @click="isEditable = true" v-else type="button">edit</button>
    <ul v-if="isEditable">
      <li>itemId: {{ item.id }}</li>
      <li>
        name:
        <input v-model="item.name" type="text" />
      </li>
      <li>
        desc:
        <textarea v-model="item.desc"></textarea>
      </li>
      <li>
        amount:
        <input v-model="item.amount" type="number" />
      </li>
      <li>
        min:
        <input v-model="item.min" type="number" />
      </li>
      <li>
        max:
        <input v-model="item.max" type="number" />
      </li>
    </ul>
    <ul v-else>
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
      isEditable: false,
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
