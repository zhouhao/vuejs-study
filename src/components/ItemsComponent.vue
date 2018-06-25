<template>
  <div>
    <item-component v-for="item in items" :key="item.text" :item="item">
    </item-component>
  </div>
</template>

<script>
  import ItemComponent from './ItemComponent'

  export default {
    name: "ItemsComponent",
    components: {ItemComponent},
    props: ['items']
  }
</script>

<style scoped>

</style>
