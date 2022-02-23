<template>
  <li>
    <div
      :class="hoverTitle ? 'item-hover' : 'item'"
      @click="toggle"
      @mouseenter="hoverTitle = true"
      @mouseleave="hoverTitle = false"
    >
      <svg
        v-if="isOpen && !isLeaf"
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-caret-down-fill"
        viewBox="0 0 16 16"
      >
        <path
          d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
        />
      </svg>

      <svg
        v-if="!isOpen && !isLeaf"
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-caret-right-fill"
        viewBox="0 0 16 16"
      >
        <path
          d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"
        />
      </svg>

      <svg
        v-if="!isLeaf && !isOpen"
        style="color: #f8d775"
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-folder-fill"
        viewBox="0 0 16 16"
      >
        <path
          d="M9.828 3h3.982a2 2 0 0 1 1.992 2.181l-.637 7A2 2 0 0 1 13.174 14H2.825a2 2 0 0 1-1.991-1.819l-.637-7a1.99 1.99 0 0 1 .342-1.31L.5 3a2 2 0 0 1 2-2h3.672a2 2 0 0 1 1.414.586l.828.828A2 2 0 0 0 9.828 3zm-8.322.12C1.72 3.042 1.95 3 2.19 3h5.396l-.707-.707A1 1 0 0 0 6.172 2H2.5a1 1 0 0 0-1 .981l.006.139z"
        />
      </svg>

      <svg
        v-if="!isLeaf && isOpen"
        style="color: #f8d775"
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-folder2-open"
        viewBox="0 0 16 16"
      >
        <path
          d="M1 3.5A1.5 1.5 0 0 1 2.5 2h2.764c.958 0 1.76.56 2.311 1.184C7.985 3.648 8.48 4 9 4h4.5A1.5 1.5 0 0 1 15 5.5v.64c.57.265.94.876.856 1.546l-.64 5.124A2.5 2.5 0 0 1 12.733 15H3.266a2.5 2.5 0 0 1-2.481-2.19l-.64-5.124A1.5 1.5 0 0 1 1 6.14V3.5zM2 6h12v-.5a.5.5 0 0 0-.5-.5H9c-.964 0-1.71-.629-2.174-1.154C6.374 3.334 5.82 3 5.264 3H2.5a.5.5 0 0 0-.5.5V6zm-.367 1a.5.5 0 0 0-.496.562l.64 5.124A1.5 1.5 0 0 0 3.266 14h9.468a1.5 1.5 0 0 0 1.489-1.314l.64-5.124A.5.5 0 0 0 14.367 7H1.633z"
        />
      </svg>

      <FileIconPicker v-if="isLeaf" :fileName="data[0]['title']" />
      <span class="ml-1" v-if="!isLeaf">{{ data[0]["title"] }}</span>
      <span class="ml-1" v-if="isLeaf">
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