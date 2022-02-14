
<template>
  <div>
    <div class="container">
      <VueDirTreeView :config="config" />
    </div>
  </div>
</template>
 
<script>
import VueDirTreeView from "./components/VueDirTreeView.vue";
import json from "./data.json";

export default {
  name: "TreeView",
  components: {
    VueDirTreeView,
  },
  data() {
    return {
      config: {
        options: {
          something: true,
        },
        data: json,
      },
    };
  },
};
</script> 