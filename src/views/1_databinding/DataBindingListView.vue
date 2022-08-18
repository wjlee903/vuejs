<template>
  <div>
    <div>
      <select name="" id="">
        <option :value="city.code" v-for="(city, index) in cities" :key="index">
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>Number</th>
            <th>Name</th>
            <th>Price</th>
            <th>Order Quantity</th>
            <th>Sum</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(drink, index) in drinkList" :key="index">
            <td>{{ drink.drinkId }}</td>
            <td>{{ drink.drinkName }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" name="" id="" v-model="drink.qty" /></td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: 'Seoul', code: '02' },
        { title: 'Busan', code: '051' },
        { title: 'Jeju', code: '064' }
      ],
      drinkList: [
        { drinkId: '1', drinkName: 'Coke', price: 700, qty: 1 },
        { drinkId: '2', drinkName: 'Juice', price: 1000, qty: 1 },
        { drinkId: '3', drinkName: 'Coffee', price: 1200, qty: 1 },
        { drinkId: '4', drinkName: 'Water', price: 1500, qty: 1 }
      ]
    }
  },
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  beforeUpdate() {},
  updated() {},
  beforeUnmount() {},
  unmounted() {},
  methods: {}
}
</script>
