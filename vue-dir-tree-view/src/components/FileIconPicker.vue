<template>
  <i>
    <svg
      v-if="fileIcon == 'word'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-word-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM5.485 6.879l1.036 4.144.997-3.655a.5.5 0 0 1 .964 0l.997 3.655 1.036-4.144a.5.5 0 0 1 .97.242l-1.5 6a.5.5 0 0 1-.967.01L8 9.402l-1.018 3.73a.5.5 0 0 1-.967-.01l-1.5-6a.5.5 0 1 1 .97-.242z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'spreadsheet'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-spreadsheet-fill"
      viewBox="0 0 16 16"
    >
      <path d="M6 12v-2h3v2H6z" />
      <path
        d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM3 9h10v1h-3v2h3v1h-3v2H9v-2H6v2H5v-2H3v-1h2v-2H3V9z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'presentation'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-easel-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M5 7.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-.5.5h-5a.5.5 0 0 1-.5-.5v-2z"
      />
      <path
        d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM8.5 6h2A1.5 1.5 0 0 1 12 7.5v2a1.5 1.5 0 0 1-1.5 1.5h-.473l.447 1.342a.5.5 0 0 1-.948.316L8.973 11H8.5v1a.5.5 0 0 1-1 0v-1h-.473l-.553 1.658a.5.5 0 1 1-.948-.316L5.973 11H5.5A1.5 1.5 0 0 1 4 9.5v-2A1.5 1.5 0 0 1 5.5 6h2a.5.5 0 0 1 1 0z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'pdf'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-pdf-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M5.523 12.424c.14-.082.293-.162.459-.238a7.878 7.878 0 0 1-.45.606c-.28.337-.498.516-.635.572a.266.266 0 0 1-.035.012.282.282 0 0 1-.026-.044c-.056-.11-.054-.216.04-.36.106-.165.319-.354.647-.548zm2.455-1.647c-.119.025-.237.05-.356.078a21.148 21.148 0 0 0 .5-1.05 12.045 12.045 0 0 0 .51.858c-.217.032-.436.07-.654.114zm2.525.939a3.881 3.881 0 0 1-.435-.41c.228.005.434.022.612.054.317.057.466.147.518.209a.095.095 0 0 1 .026.064.436.436 0 0 1-.06.2.307.307 0 0 1-.094.124.107.107 0 0 1-.069.015c-.09-.003-.258-.066-.498-.256zM8.278 6.97c-.04.244-.108.524-.2.829a4.86 4.86 0 0 1-.089-.346c-.076-.353-.087-.63-.046-.822.038-.177.11-.248.196-.283a.517.517 0 0 1 .145-.04c.013.03.028.092.032.198.005.122-.007.277-.038.465z"
      />
      <path
        fill-rule="evenodd"
        d="M4 0h5.293A1 1 0 0 1 10 .293L13.707 4a1 1 0 0 1 .293.707V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2zm5.5 1.5v2a1 1 0 0 0 1 1h2l-3-3zM4.165 13.668c.09.18.23.343.438.419.207.075.412.04.58-.03.318-.13.635-.436.926-.786.333-.401.683-.927 1.021-1.51a11.651 11.651 0 0 1 1.997-.406c.3.383.61.713.91.95.28.22.603.403.934.417a.856.856 0 0 0 .51-.138c.155-.101.27-.247.354-.416.09-.181.145-.37.138-.563a.844.844 0 0 0-.2-.518c-.226-.27-.596-.4-.96-.465a5.76 5.76 0 0 0-1.335-.05 10.954 10.954 0 0 1-.98-1.686c.25-.66.437-1.284.52-1.794.036-.218.055-.426.048-.614a1.238 1.238 0 0 0-.127-.538.7.7 0 0 0-.477-.365c-.202-.043-.41 0-.601.077-.377.15-.576.47-.651.823-.073.34-.04.736.046 1.136.088.406.238.848.43 1.295a19.697 19.697 0 0 1-1.062 2.227 7.662 7.662 0 0 0-1.482.645c-.37.22-.699.48-.897.787-.21.326-.275.714-.08 1.103z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'image'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-image-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M4 0h5.293A1 1 0 0 1 10 .293L13.707 4a1 1 0 0 1 .293.707v5.586l-2.73-2.73a1 1 0 0 0-1.52.127l-1.889 2.644-1.769-1.062a1 1 0 0 0-1.222.15L2 12.292V2a2 2 0 0 1 2-2zm5.5 1.5v2a1 1 0 0 0 1 1h2l-3-3zm-1.498 4a1.5 1.5 0 1 0-3 0 1.5 1.5 0 0 0 3 0z"
      />
      <path
        d="M10.564 8.27 14 11.708V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2v-.293l3.578-3.577 2.56 1.536 2.426-3.395z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'code-js'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-filetype-js"
      viewBox="0 0 16 16"
    >
      <path
        fill-rule="evenodd"
        d="M14 4.5V14a2 2 0 0 1-2 2H8v-1h4a1 1 0 0 0 1-1V4.5h-2A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v9H2V2a2 2 0 0 1 2-2h5.5L14 4.5ZM3.186 15.29a1.176 1.176 0 0 1-.111-.449h.765a.578.578 0 0 0 .255.384c.07.049.153.087.249.114.095.028.202.041.319.041.164 0 .302-.023.413-.07a.559.559 0 0 0 .255-.193.507.507 0 0 0 .085-.29.387.387 0 0 0-.153-.326c-.101-.08-.255-.144-.462-.193l-.619-.143a1.72 1.72 0 0 1-.539-.214 1.001 1.001 0 0 1-.351-.367 1.068 1.068 0 0 1-.123-.524c0-.244.063-.457.19-.639.127-.181.303-.322.528-.422.224-.1.483-.149.776-.149.305 0 .564.05.78.152.216.102.383.239.5.41.12.17.186.359.2.566h-.75a.56.56 0 0 0-.12-.258.624.624 0 0 0-.247-.181.923.923 0 0 0-.369-.068c-.217 0-.388.05-.513.152a.472.472 0 0 0-.184.384c0 .121.048.22.143.3a.97.97 0 0 0 .405.175l.62.143c.218.05.406.12.566.211.16.09.285.21.375.358.09.148.135.335.135.56 0 .247-.063.466-.188.656a1.216 1.216 0 0 1-.539.439c-.234.105-.52.158-.858.158-.254 0-.476-.03-.665-.09a1.404 1.404 0 0 1-.478-.252 1.13 1.13 0 0 1-.29-.375Zm-3.104-.033A1.32 1.32 0 0 1 0 14.791h.765a.576.576 0 0 0 .073.27.499.499 0 0 0 .454.246c.19 0 .33-.055.422-.164.092-.11.138-.265.138-.466v-2.745h.79v2.725c0 .44-.119.774-.357 1.005-.236.23-.564.345-.984.345a1.59 1.59 0 0 1-.569-.094 1.145 1.145 0 0 1-.407-.266 1.14 1.14 0 0 1-.243-.39Z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'code-php'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-filetype-php"
      viewBox="0 0 16 16"
    >
      <path
        fill-rule="evenodd"
        d="M14 4.5V14a2 2 0 0 1-2 2h-1v-1h1a1 1 0 0 0 1-1V4.5h-2A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v9H2V2a2 2 0 0 1 2-2h5.5L14 4.5ZM1.6 11.85H0v3.999h.791v-1.342h.803c.287 0 .531-.057.732-.173.203-.117.358-.275.463-.474a1.42 1.42 0 0 0 .161-.677c0-.25-.053-.476-.158-.677a1.176 1.176 0 0 0-.46-.477c-.2-.12-.443-.179-.732-.179Zm.545 1.333a.795.795 0 0 1-.085.38.574.574 0 0 1-.238.241.794.794 0 0 1-.375.082H.788V12.48h.66c.218 0 .389.06.512.181.123.122.185.295.185.522Zm4.48 2.666V11.85h-.79v1.626H4.153V11.85h-.79v3.999h.79v-1.714h1.682v1.714h.79Zm.703-3.999h1.6c.288 0 .533.06.732.179.2.117.354.276.46.477.105.201.158.427.158.677 0 .25-.054.476-.161.677-.106.199-.26.357-.463.474a1.452 1.452 0 0 1-.733.173H8.12v1.342h-.791V11.85Zm2.06 1.714a.795.795 0 0 0 .084-.381c0-.227-.061-.4-.184-.521-.123-.122-.294-.182-.513-.182h-.66v1.406h.66a.794.794 0 0 0 .375-.082.574.574 0 0 0 .237-.24Z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'code'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-code-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM6.646 7.646a.5.5 0 1 1 .708.708L5.707 10l1.647 1.646a.5.5 0 0 1-.708.708l-2-2a.5.5 0 0 1 0-.708l2-2zm2.708 0 2 2a.5.5 0 0 1 0 .708l-2 2a.5.5 0 0 1-.708-.708L10.293 10 8.646 8.354a.5.5 0 1 1 .708-.708z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'video'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-play-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM6 6.883a.5.5 0 0 1 .757-.429l3.528 2.117a.5.5 0 0 1 0 .858l-3.528 2.117a.5.5 0 0 1-.757-.43V6.884z"
      />
    </svg>
    <svg
      v-if="fileIcon == 'unknown'"
      :style="style"
      xmlns="http://www.w3.org/2000/svg"
      width="16"
      height="16"
      fill="currentColor"
      class="bi bi-file-earmark-break-fill"
      viewBox="0 0 16 16"
    >
      <path
        d="M4 0h5.293A1 1 0 0 1 10 .293L13.707 4a1 1 0 0 1 .293.707V9H2V2a2 2 0 0 1 2-2zm5.5 1.5v2a1 1 0 0 0 1 1h2l-3-3zM2 12h12v2a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2v-2zM.5 10a.5.5 0 0 0 0 1h15a.5.5 0 0 0 0-1H.5z"
      />
    </svg>
  </i>
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
      fileIcon: "bi bi-folder-fill",
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
        this.style.color = "#1b7ced";
        this.fileIcon = "word";
      } else if (
        // Spreadsheets
        this.fileName.endsWith(".xlsx") ||
        this.fileName.endsWith(".csv") ||
        this.fileName.endsWith(".xls") ||
        this.fileName.endsWith(".ods")
      ) {
        this.style.color = "#1d6f42";
        this.fileIcon = "spreadsheet";
      } else if (
        // Power point
        this.fileName.endsWith(".bmp") ||
        this.fileName.endsWith(".ppsx") ||
        this.fileName.endsWith(".pptx") ||
        this.fileName.endsWith(".ppt")
      ) {
        this.style.color = "#d04423";
        this.fileIcon = "presentation";
      } else if (
        // Images
        this.fileName.endsWith(".jpg") ||
        this.fileName.endsWith(".img") ||
        this.fileName.endsWith(".png") ||
        this.fileName.endsWith(".svg") ||
        this.fileName.endsWith(".gif") ||
        this.fileName.endsWith(".tiff")
      ) {
        this.style.color = "#8C9C16";
        this.fileIcon = "image";
      } else if (
        // Images
        this.fileName.endsWith(".mp3") ||
        this.fileName.endsWith(".mov") ||
        this.fileName.endsWith(".wmv") ||
        this.fileName.endsWith(".avi") ||
        this.fileName.endsWith(".avchd") ||
        this.fileName.endsWith(".mkv") ||
        this.fileName.endsWith(".f4v") ||
        this.fileName.endsWith(".fls")
      ) {
        this.style.color = "#154FB5";
        this.fileIcon = "video";
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
        this.style.color = "#15B59F";
        this.fileIcon = "code";
      } else if (this.fileName.endsWith(".js")) {
        // Javascript
        this.style.color = "#fdb813";
        this.fileIcon = "code-js";
      } else if (this.fileName.endsWith(".php")) {
        // PHP
        this.style.color = "#474A8A";
        this.fileIcon = "code-php";
      } else if (this.fileName.endsWith(".pdf")) {
        // Pdf
        this.style.color = "#ff0000";
        this.fileIcon = "pdf";
      } else {
        this.style.color = "#000";
        this.fileIcon = "unknown";
      }
    },
  },
};
</script>