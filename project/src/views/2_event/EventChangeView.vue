<template>
  <div>
    <select name="" id="" @click="changeCity($event)" v-model="selectedCity">
      <option>==도시선택==</option>
      <option
        :value="city.cityCode"
        :key="city.cityCode"
        v-for="city in cityList"
      >
        {{ city.title }}
      </option>
    </select>
    <select name="" id="">
      <option
        :key="dong.dongCode"
        :value="idx"
        v-for="(dong, idx) in selectedDongList"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
    <select name="" id="">
      <option
        v-for="dong in dongList.filter(
          (dong) => dong.cityCode === selectedCity
        )"
        :key="dong.dongCode"
        :value="dong.dongCode"
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
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '051', title: '부산' },
        { cityCode: '064', title: '제주' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울 1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울 2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울 3동' },
        { cityCode: '02', dongCode: '4', dongTitle: '서울 4동' },
        { cityCode: '051', dongCode: '1', dongTitle: '부산 1동' },
        { cityCode: '051', dongCode: '2', dongTitle: '부산 2동' },
        { cityCode: '051', dongCode: '3', dongTitle: '부산 3동' },
        { cityCode: '064', dongCode: '1', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '2', dongTitle: '제주 2동' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log(event)
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>
