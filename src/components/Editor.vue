<template>
<div>
  <div id="codex-editor"></div>
</div>
</template>

<script>

  import EditorJS from "@editorjs/editorjs";
  import Header from "@editorjs/header";
  import List from "@editorjs/list";
  import Checklist from "@editorjs/checklist";

  export default {
    name: "Editor",

    data() {
      return {
        editor: undefined
      }
    },

    mounted() {

      this.editor = new EditorJS({
        autofocus: true,
        holderId: "codex-editor",
        tools: {
          header: {
            class: Header,
            inlineToolbar: true,
            shortcut: 'CMD+SHIFT+H'
          },
          checklist: {
            class: Checklist,
            inlineToolbar: true
          },
        }
      });
    }



  }

</script>