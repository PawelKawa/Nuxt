<template>
    <div>
        <p>ckeditor classic</p>
        <ckeditor :editor="editor" v-model="editorData" :config="editorConfig"></ckeditor>
        <p>{{ editorData }}</p>
    </div>
</template>

<script>
import Vue from 'vue';
import CKEditor from '@ckeditor/ckeditor5-vue2';
import ClassicEditor from '@ckeditor/ckeditor5-build-classic';
Vue.use( CKEditor );

export default {
        name: 'app',
        data() {
            return {
                editor: ClassicEditor,
                editorData: '<p>Content of the editor.</p>',
                editorConfig: {
                    // The configuration of the editor.
                    toolbar: {
                        items: [
                            'bold',
                            'italic',
                            'link',
                            'undo',
                            'redo',
                        ]
                    }
                }
            };
        }
    }
</script>