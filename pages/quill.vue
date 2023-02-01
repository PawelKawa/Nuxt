<template>
   <div>
    <client-only placeholder="loading...">
       <vue-editor :editorToolbar="customToolbar" v-model="content"></vue-editor>
    </client-only>
       <p>asd</p>
   </div>
  </template>
  
  <script>
    import { VueEditor } from 'vue2-quill-editor'
  
    export default {
  
    components: {
       VueEditor
    },
  
    data() {
        return {
          content: 'Some initial content',
          customToolbar: [
            ['bold', 'italic', 'underline'],
            [{ 'list': 'ordered' }, { 'list': 'bullet' }],
            [],
          ]  
        }
      }
    }
  </script> 