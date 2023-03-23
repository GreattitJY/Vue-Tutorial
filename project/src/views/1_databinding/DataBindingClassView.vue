<template>
  <div>
    <div :class="{'text-red': hasError, active: isActive}" @click="toggle">클래스 바인딩</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      hasError: false
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    toggle() {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style>
  .active {
    box-shadow: inset 0 0 1px blue;
  }
  .text-red {
    color: red;
  }
</style>
