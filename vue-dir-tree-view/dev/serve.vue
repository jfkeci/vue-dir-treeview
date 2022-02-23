<script>
import Vue from 'vue';
import VueDirTreeView from '@/vue-dir-tree-view.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueDirTreeView
  }
});
</script>

<template>
  <div id="app">
    <vue-dir-tree-view />
  </div>
</template>
