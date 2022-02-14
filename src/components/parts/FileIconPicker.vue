<template>
  <b-icon :icon="fileIcon" :style="style"></b-icon>
</template>


<script>
export default {
  name: "FileIconPicker",
  props: {
    fileName: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      fileIcon: "folder-fill",
      style: {
        color: "#fdb813",
      },
    };
  },
  created() {
    this.checkIcon();
  },
  methods: {
    checkIcon() {
      if (
        // Word documents
        this.fileName.endsWith(".docx") ||
        this.fileName.endsWith(".doc") ||
        this.fileName.endsWith(".rtf") ||
        this.fileName.endsWith(".odt")
      ) {
        this.style = { color: "#1b7ced" };
        this.fileIcon = "file-earmark-word-fill";
      } else if (
        // Spreadsheets
        this.fileName.endsWith(".xlsx") ||
        this.fileName.endsWith(".csv") ||
        this.fileName.endsWith(".xls") ||
        this.fileName.endsWith(".ods")
      ) {
        this.style = { color: "#1d6f42" };
        this.fileIcon = "file-earmark-spreadsheet-fill";
      } else if (
        // Power point
        this.fileName.endsWith(".bmp") ||
        this.fileName.endsWith(".ppsx") ||
        this.fileName.endsWith(".pptx") ||
        this.fileName.endsWith(".ppt")
      ) {
        this.style = { color: "#d04423" };
        this.fileIcon = "file-earmark-easel-fill";
      } else if (
        // Images
        this.fileName.endsWith(".jpg") ||
        this.fileName.endsWith(".img") ||
        this.fileName.endsWith(".png") ||
        this.fileName.endsWith(".svg") ||
        this.fileName.endsWith(".gif") ||
        this.fileName.endsWith(".tiff")
      ) {
        this.style = { color: "#8C9C16" };
        this.fileIcon = "file-image-fill";
      } else if (
        // Programming
        this.fileName.endsWith(".vue") ||
        this.fileName.endsWith(".ts") ||
        this.fileName.endsWith(".html") ||
        this.fileName.endsWith(".css") ||
        this.fileName.endsWith(".sh") ||
        this.fileName.endsWith(".c") ||
        this.fileName.endsWith(".cs") ||
        this.fileName.endsWith(".cpp")
      ) {
        this.style = { color: "#15B59F" };
        this.fileIcon = "file-earmark-binary-fill";
      } else if (this.fileName.endsWith(".js")) {
        // Javascript
        this.style = { color: "#fdb813" };
        this.fileIcon = "file-earmark-code-fill";
      } else if (this.fileName.endsWith(".php")) {
        // PHP
        this.style = { color: "#474A8A" };
        this.fileIcon = "file-earmark-code-fill";
      } else if (this.fileName.endsWith(".pdf")) {
        // Pdf
        this.style = { color: "#ff0000" };
        this.fileIcon = "file-earmark-post";
      } else {
        this.style = { color: "#000" };
        this.fileIcon = "file-earmark-fill";
      }
    },
  },
};
</script>