<template>
  <li :class="{ 'removed': item.checked }">
    <div class="checkbox">
      <label>
        <input type="checkbox" v-model="item.checked"> {{ item.text }}
      </label>
    </div>
  </li>
</template>

<script>
  export default {
    name: "ItemComponent",
    props: ['item']
  }
</script>

<style lang="scss" scoped>
  .removed {
    color: gray;

    span {
      text-decoration: line-through;
    }
  }

  li {
    list-style-type: none;
    span {
      margin-left: 5px;
    }
  }
</style>
