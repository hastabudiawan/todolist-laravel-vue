<template>
  <div>
    <div v-for="(item, index) in items" :key="index">
      <list-item
        :item="item"
        class="item"
        v-on:itemchanged="$emit('reloadlist')"
      />
    </div>
  </div>
</template>

<script>
import listItem from "./listItem";
export default {
  props: ["items"],
  components: {
    listItem,
  },
};
</script>

<style scoped>
.item {
  background: #f36c21;
  padding: 5px;
  margin-top: 5px;
  height: 30px;
  border-radius: 10px;
}
</style>