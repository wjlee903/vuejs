<template>
  <div>
    <!-- 단어로만 이루어진 클래스명에서는 저장 시 홑따옴표로 저장됨 -->
    <div :class="{ 'text-red': isActive, active: hasError }">
      Class Binding 1
    </div>
    <button @click=";(isActive = true), (hasError = true)">True</button>
    <button @click=";(isActive = false), (hasError = false)">False</button>
    <hr />
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      isActive: true,
      hasError: true
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
.active {
  background-color: cyan;
  font-weight: bold;
}
.text-red {
  color: red;
}
</style>
