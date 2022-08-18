<template>
  <div>
    <h1>Hello, {{ username }}</h1>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: 'Hello',
      message: 'Welcome Vue Study',
      arr: [],
      obf: {}
    }
  }
}
</script>

<style scoped>
.text-red{
    color: red;
}
</style>
