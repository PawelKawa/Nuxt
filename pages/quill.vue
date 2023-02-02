<template>
  <!DOCTYPE html>
   <div>

    <client-only placeholder="loading...">
       <vue-editor :editorToolbar="customToolbar" v-model="content"></vue-editor>
    </client-only>

       <span class="katex">
        <span class="katex-mathml">The KaTeX stylesheet is not loaded!</span>
        <span class="katex-version rule">KaTeX stylesheet version: </span>
      </span>

   </div>
  </template>
  
  <script>
    import { VueEditor } from 'vue2-quill-editor';
    import { katex } from 'katex';
    import 'katex/dist/katex.min.css';

    export default {
  
    components: {
       VueEditor, katex
    },
  
    data() {
        return {
          content: 'Some initial content',
          customToolbar: [
            ['bold', 'italic', 'underline'],
            [{ 'list': 'ordered' }, { 'list': 'bullet' }],
            ['formula'],
          ],
        }
      }
    }
  </script> 

<style>
.katex-version {display: none;}
.katex-version::after {content:"0.10.2 or earlier";}
</style>