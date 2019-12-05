<template>
  <div class="register-item">
    <h2>RegisterItem</h2>
    <section>
      <button type="button">save</button>
      <ul>
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
          {{ deficientNumber }}
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
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      item: {
        id: null,
        name: '',
        desc: '',
        left: 0,
        idealLeft: 0,
        buyDate: this.$dayjs().format('YYYY-MM-DDThh:mm:ss'),
        bestByDate: this.$dayjs().format('YYYY-MM-DDThh:mm:ss'),
        expiryDate: this.$dayjs().format('YYYY-MM-DDThh:mm:ss'),
        expectedDigestionDays: 0
      }
    }
  },
  computed: {
    deficientNumber() {
      return this.item.idealLeft - this.item.left
    }
  }
}
</script>
