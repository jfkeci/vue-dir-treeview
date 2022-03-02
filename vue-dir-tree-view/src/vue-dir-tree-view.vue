<template>
  <div>
    <ul style="list-style: none">
      <TreeListItem :options="config.options" :data="config.data" @item-click="onClick" />
    </ul>
  </div>
</template>

<script>
import TreeListItem from "./components/TreeListItem";
export default {
  name: "VueDirTreeView",
  components: {
    TreeListItem,
  },
  props: {
    config: {
      type: Object,
      required: true,
    },
  },
  methods:{
    onClick(item){
      this.$emit('item-click', item)
    }
  }
};
</script>

<style scoped>
.item {
  cursor: pointer;
}
.bold {
  font-weight: bold;
}
ul {
  padding-left: 1em;
  line-height: 1.5em;
  list-style-type: dot;
}
</style>