<template>
  <div>
    <client-only placeholder="loading...">
      <vue-editor :editorToolbar="customToolbar" v-model="content"></vue-editor>
    </client-only>

    <p>{{ content }}</p>
    <p>{{ content.length }} chars</p>
    <p v-html="content"></p>

    <button @click="saveContent">renderToString?</button>
    <span class="katex">
      <span class="katex-mathml">The KaTeX stylesheet is not loaded!</span>
      <span class="katex-version rule">KaTeX stylesheet version: </span>
    </span>

  </div>
</template>

<script>
import { VueEditor } from "vue2-quill-editor";
import katex from "katex";
import "katex/dist/katex.min.css";

export default {
  components: {
    VueEditor,
  },

  data() {
    return {
      content: "a^2+b^2=c^2",
      customToolbar: [
        ["bold", "italic", "underline"],
        [{ list: "ordered" }, { list: "bullet" }],
        ["formula"],
      ],
      
    };
  },
  methods: {
    saveContent: function() {
      let latex = "a^2+b^2=c^2";
      let html = katex.renderToString(latex);
      this.content = html;
      }
    },
  mounted() {
    window.katex = katex;
  },
};
</script>

<style>
.katex-version {
  display: none;
}
.katex-version::after {
  content: "0.10.2 or earlier";
}
</style>
