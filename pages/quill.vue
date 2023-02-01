<template>
   <div>
    <client-only placeholder="loading...">
       <vue-editor v-model="content"></vue-editor>
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
          content: '<h1>Some initial content</h1>'  
        }
      }
    }
  </script> 