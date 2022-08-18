<template>
  <div>
    <input type="text" name="" id="" v-bind:value="userId" readonly />
    <br />
    <input type="text" name="" id="" :value="userId" readonly />
    <hr>
    <img :src="imgSrc" alt="" style="width: 100px; height: auto" />
    <hr>
    <input type="search" v-model="txt1" >
    <button :disabled="txt1 === ''">Search</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'silverbell',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/2367px-Vue.js_Logo_2.svg.png',
      txt1: ''
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
