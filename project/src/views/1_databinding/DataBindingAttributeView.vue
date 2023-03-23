<template>
  <div>
    <input type="text" v-bind:value="userId" readonly>
    <input type="text" :value="userId" readonly>
    <br>
    <br>
    <img :src="imgSrc" alt="" style="width:100px; height:auto;">
    <input type="search" v-model="txt1">
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      userId: '',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1200px-Vue.js_Logo_2.svg.png',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
