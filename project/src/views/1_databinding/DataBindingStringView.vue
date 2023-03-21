<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p class="text-blue">{{ message }}</p>
  </div>
</template>

<script>

export default {
  data() {
    return {
      userName: 'John Doe',
      message: 'welcome vue start',
      arr: [],
      obj: {}
    }
  }
}
</script>

<style scoped>
.text-blue {
  color: blue;
}
</style>
