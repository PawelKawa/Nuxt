<template>
    <div>
        <hr>
        <p>ckeditor</p>
      <client-only placeholder="loading...">
        <ckeditor-nuxt v-model="contentHolder" :config="editorConfig" />
      </client-only>
    <p class="text-right mt-2">{{ contentHolder.length }}/555</p>
    </div>
  </template>
  
  <script>
  export default {
    components: {
      "ckeditor-nuxt": () => {
        if (process.client) {
          return import("@blowstack/ckeditor-nuxt");
        }
      },
    },
    data() {
      return {
          editorConfig: {
          toolbar:["SpecialCharacters","MathType",],
          removePlugins: [
            "Title",
          //   "RemoveFormat",
          //   "Heading",
          //   "FontFamily",
          //   "FontColor",
          //   "FontBackgroundColor",
          //   "Highlight",
          //   "CodeBlock",
          //   "BlockQuote",
          //   "PageBreak",
          //   "Table",
          //   "Bold",
          //   "Italic",
          //   "Underline",
          //   "Strikethrough",
          //   "Code",
          //   "Alignment",
          //   "IndentBlock",
          //   "Indent",
          //   "ListStyle",
          //   "List",
          //   "ListEditing",
          //   "ListProperties",
          //   "ListPropertiesEditing",
          //   "ListPropertiesUI",
          //   "ListStyle",
          //   "ListUI",
          //   "ListUtils",
          //   "TodoList",
          //   "ImageBlock",
          //   "ImageBlockEditing",
          //   "ImageCaption",
          //   "ImageCaptionEditing",
          //   "ImageCaptionUI",
          //   "ImageCaptionUtils",
          //   "ImageEditing",
          //   "ImageElementSupport",
          //   "ImageInline",
          //   "ImageInlineEditing",
          //   "ImageInsert",
          //   "ImageInsertUI",
          //   "ImageInsertViaUrl",
          //   "ImageResize",
          //   "ImageResizeButtons",
          //   "ImageResizeEditing",
          //   "ImageResizeHandles",
          //   "ImageStyle",
          //   "ImageStyleEditing",
          //   "ImageStyleUI",
          //   "ImageTextAlternative",
          //   "ImageTextAlternativeEditing",
          //   "ImageTextAlternativeUI",
          //   "ImageToolbar",
          //   "ImageUpload",
          //   "ImageUploadEditing",
          //   "ImageUploadProgress",
          //   "ImageUploadUI",
          //   "ImageUtils",
          //   "Image",
          //   "LinkImageEditing",
          //   "LinkImage",
          //   "Link",
          //   "LinkEditing",
          //   "LinkImageEditing",
          //   "LinkImageUI",
          //   "LinkUI",
          //   "HorizontalLine",
          //   "FontSize",
          ],
          placeholder: "Description...",
        },
        contentHolder: "",
      };
    },
  };
  </script>
