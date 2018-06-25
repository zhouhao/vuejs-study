<template>
  <div>
    <div class="input-group">
      <input type="text" v-model="newItem" class="input form-control" placeholder="add shopping list item">
      <span class="input-group-btn">
        <button  v-on:click="addItem" class="btn btn-default" type="button">Add!</button>
      </span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "AddItemComponent",
    data: function () {
      return {
        newItem: ''
      }
    },
    props: ['items'],
    methods: {
      addItem: function () {
        var text = this.newItem.trim();
        if (text) {
          this.items.push({
            text: text,
            checked: false
          });
          this.newItem = '';
        }
      }
    }
  }
</script>

<style scoped>

</style>
