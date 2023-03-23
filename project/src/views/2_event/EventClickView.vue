<template>
  <div>
    <button @click="increateCounter">Add1</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      counter: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increateCounter() {
      this.counter += 1
    }
  }
}
</script>
