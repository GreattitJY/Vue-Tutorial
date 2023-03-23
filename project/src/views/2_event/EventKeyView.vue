<template>
  <div>
    <!-- <input
      type="search"
      name=""
      id=""
      v-model="searchText"
      @keyup="checkEnter($event)"
    /> -->
    <form>
      <input
        type="search"
        name=""
        id=""
        v-model="searchText"
        @keyup.enter="doSearch($event)"
      />
      <!-- <button @click="doSearch($event)">조회</button> -->
      <button @click.prevent="doSearch($event)">조회</button>
    </form>
  </div>
</template>

<script>
// .enter
// .tab
// .delete
// .esc
// .up
// .down
// .left
// .right
// .stop - event.stopPropagation();
// .prevent - event.preventDeafault();
export default {
  components: {},
  data() {
    return {
      searchText: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    doSearch(event) {
      // event.preventDefault()
      console.log(this.searchText)
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>
