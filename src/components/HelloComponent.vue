<template>
  <h1>{{ msg }}</h1>
</template>

<script>
  export default {
    name: "HelloComponent",
    data: () => {
      return {msg: "hello"};
    }
  }
</script>

<style lang="scss" scoped>
  $red: red;
  h1 {
    color: $red;
  }
</style>
