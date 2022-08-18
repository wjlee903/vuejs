<template>
  <div>
    <div style="color: red; font-size: 30px">
      Style Binding : Color red, Font-size 30px
    </div>
    <div :style="style1">Style Binding : Color red, Font-size 30px</div>
    <button @click="style1.color = bule">Change Color Blue</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: 'green',
        fontSize: '30px'
      }
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

<style scoped>
</style>
