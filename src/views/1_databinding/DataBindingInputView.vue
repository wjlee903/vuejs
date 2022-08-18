<template>
  <div>
    <div>{{ userId }}</div>
    <input type="text" v-model="userId" />
    <div>
      <button @click="myFunction1">Change Hello</button>
      <button @click="myFunction2">Change World</button>
    </div>
    <hr>
    <input type="text" v-model="num1" /> +
    <input type="text" v-model="num2" /> =
    <span>{{ num1 + num2 }}</span>
    <hr>
    <input type="text" v-model.number="num3" /> +
    <input type="text" v-model.number="num4" /> =
    <span>{{ num3 + num4 }}</span>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'Vue.js',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0
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
  methods: {
    myFunction1() {
      this.userId = 'Hello'
    },
    myFunction2() {
      this.userId = 'World'
    }
  }
}
</script>
