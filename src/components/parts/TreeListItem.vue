<template>
  <li>
    <div
      :class="hoverTitle ? 'item-hover' : 'item'"
      @click="toggle"
      @mouseenter="hoverTitle = true"
      @mouseleave="hoverTitle = false"
    >
      <b-icon-caret-right-fill v-if="!isOpen && !isLeaf" />
      <b-icon-caret-down-fill v-if="isOpen && !isLeaf" />
      <b-icon-folder-fill v-if="!isLeaf && !isOpen" style="color: #f8d775" />
      <b-icon-folder2-open v-if="!isLeaf && isOpen" style="color: #f8d775" />
      <FileIconPicker v-if="isLeaf" :fileName="data[0]['title']" />
      <span v-if="!isLeaf">{{ data[0]["title"] }}</span>
      <span v-if="isLeaf">
        {{ trimText(data[0]["title"]) }}
      </span>
      <!-- <b-icon-download
        size="sm"
        v-if="isLeaf"
        class="ml-2"
        style="color: #000"
        @click="download(data[0]['id'])"
      /> -->
    </div>
    <ul v-show="isOpen" style="list-style: none">
      <TreeListItem
        v-for="(child, index) in data[0]['children']"
        :key="index"
        :data="[child]"
        :options="options"
      />
    </ul>
  </li>
</template>

<script>
import TreeListItem from "./TreeListItem";
import FileIconPicker from "./FileIconPicker";
export default {
  name: "TreeListItem",
  components: {
    TreeListItem,
    FileIconPicker,
  },
  props: {
    options: {
      type: Object,
      required: true,
    },
    data: {
      required: true,
    },
  },
  data() {
    return {
      isOpen: false,
      hoverTitle: false,
    };
  },
  computed: {
    isLeaf() {
      return this.data[0]["isLeaf"];
    },
  },
  methods: {
    toggle() {
      if (!this.data[0]["isLeaf"]) {
        this.isOpen = !this.isOpen;
      }
    },
    trimText(text) {
      if (text.length > 20) {
        let length = text.length;
        let trimmed =
          text.substr(0, 11 - 1) + "..." + text.substr(length - 7, length - 1);
        return trimmed;
      } else {
        return text;
      }
    },
  },
};
</script>

<style scoped>
.bold {
  color: #337ab7 !important;
}
.tree-node {
  cursor: pointer;
}

.item {
  cursor: pointer;
  margin: 2px;
}

.item-hover {
  color: #337ab7;
  cursor: pointer;
  border-style: solid;
  border-width: thin;
  border-radius: 4px;
}
</style>