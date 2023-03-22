<template>
  <div>
    <form>
      <fieldset>
        <!-- checkbox에서 v-model은 value랑 직접 연결된 게 아니라 input 태그 안에 checked라는 속성과 연결돼서 value의 값을 읽어오는 것 -->
        <input type="checkbox" name="" id="html" value="HTML" v-model="favoriteLang">
        <label for="html">HTML</label>
      </fieldset>
      <fieldset>
        <input type="checkbox" name="" id="css" value="CSS" v-model="favoriteLang">
        <label for="css">CSS</label>
      </fieldset>
      <fieldset>
        <input type="checkbox" name="" id="javascript" value="javascript" v-model="favoriteLang">
        <label for="javascript">JavaScript</label>
      </fieldset>
    </form>
    <div>선택한 지역 : {{ favoriteLang }}</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      favoriteLang: ['javascript']
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>

<style scoped="">
  fieldset {
    border: none;
  }
</style>
