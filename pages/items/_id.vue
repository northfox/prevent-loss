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
        left:
        <input v-model="item.left" type="number" />
      </li>
      <li>
        idealLeft:
        <input v-model="item.idealLeft" type="number" />
      </li>
      <li>
        deficientNumber:
        <input v-model="item.deficientNumber" type="number" />
      </li>
      <li>
        buyDate:
        <input v-model="item.buyDate" type="datetime-local" />
      </li>
      <li>
        bestByDate:
        <input v-model="item.bestByDate" type="datetime-local" />
      </li>
      <li>
        expiryDate:
        <input v-model="item.expiryDate" type="datetime-local" />
      </li>
      <li>
        expectedDigestionDays:
        <input v-model="item.expectedDigestionDays" type="number" />
      </li>
    </ul>
    <ul v-else>
      <li>itemId: {{ item.id }}</li>
      <li>name: {{ item.name }}</li>
      <li>desc: {{ item.desc }}</li>
      <li>left: {{ item.left }}</li>
      <li>min: {{ item.idealLeft }}</li>
      <li>max: {{ item.deficientNumber }}</li>
      <li>max: {{ item.buyDate }}</li>
      <li>max: {{ item.bestByDate }}</li>
      <li>max: {{ item.expiryDate }}</li>
      <li>max: {{ item.expectedDigestionDays }}</li>
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
        left: 100,
        idealLeft: 150,
        // deficientNumber: this.item.idealLeft - this.item.left,
        buyDate: this.$dayjs().format('YYYY-MM-DD'),
        bestByDate: this.$dayjs().format('YYYY-MM-DD'),
        expiryDate: this.$dayjs().format('YYYY-MM-DD'),
        expectedDigestionDays: 5
      }
    }
  }
}
</script>
