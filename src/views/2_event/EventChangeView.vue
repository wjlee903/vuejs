<template>
  <div>
    <select name="" id="" @change="changeCity($event)" v-model="selectedCity">
      <option value="">CIty Select</option>
      <option :value="city.cityCode" v-for="(city, i) in citiList" :key="i">
        {{ city.title }}
      </option>
    </select>
    <hr />
    <select name="" id="" v-model="selectedCity">
      <option value="">CIty Select</option>
      <option :value="city.cityCode" v-for="(city, i) in citiList" :key="i">
        {{ city.title }}
      </option>
    </select>
    <hr />
    <select name="" id="">
      <option
        value="dong.dongCode"
        v-for="(dong, i) in selelctedDongList"
        :key="i"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
    <hr />
    <select name="" id="">
      <option
        value="dong.dongCode"
        v-for="(dong, i) in dongList.filter(
          (dong) => dong.cityCode === selectedCity
        )"
        :key="i"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      citiList: [
        { cityCode: '02', title: 'Seoul' },
        { cityCode: '051', title: 'Busan' },
        { cityCode: '064', title: 'Jeju' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: 'Seoul 1 dong' },
        { cityCode: '02', dongCode: '2', dongTitle: 'Seoul 2 dong' },
        { cityCode: '02', dongCode: '3', dongTitle: 'Seoul 3 dong' },
        { cityCode: '02', dongCode: '4', dongTitle: 'Seoul 4 dong' },
        { cityCode: '051', dongCode: '1', dongTitle: 'Busan 1 dong' },
        { cityCode: '051', dongCode: '2', dongTitle: 'Busan 2 dong' },
        { cityCode: '051', dongCode: '3', dongTitle: 'Busan 3 dong' },
        { cityCode: '051', dongCode: '4', dongTitle: 'Busan 4 dong' },
        { cityCode: '064', dongCode: '1', dongTitle: 'Jeju 1 dong' },
        { cityCode: '064', dongCode: '2', dongTitle: 'Jeju 2 dong' },
        { cityCode: '064', dongCode: '3', dongTitle: 'Jeju 3 dong' },
        { cityCode: '064', dongCode: '4', dongTitle: 'Jeju 4 dong' }
      ],
      selelctedDongList: [],
      selectedCity: ''
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
    changeCity(event) {
      console.log(event.target.tagName)
      this.selelctedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>
