<template>

  <div>
    <Title></Title>
    <md-editor v-model="text"
               :language="language"
               :languageUserDefined="languageUserDefined"
               :marked-heading="markedHeading"
               @onGetCatalog="onGetCatalog"
               :sanitize="sanitize"
               :toolbars="toolbars"


    />

  </div>


</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import MdEditor from 'md-editor-v3';
import 'md-editor-v3/lib/style.css';
import sanitizeHtml from 'sanitize-html';



export default defineComponent({
  components: { MdEditor },
  data(){
    return{
      catalogList: [],
      toolbars: ['bold','underline', 'italic','strikeThrough', '-','title','sub','sup','quote','unorderedList','orderedList','-','codeRow','code','link','image','table','mermaid','katex','-','revoke','next','save', '=', 'prettier','pageFullscreen','fullscreen','preview','catalog']
    }
  },
  methods:{
    sanitize(html) { return sanitizeHtml(html) },
    onGetCatalog(list) {
      this.catalogList = list
    },

    markedHeading(text, level, raw) {
      // 你不能直接调用默认的markedHeadingId，但是它很简单
      // 如果你的id与raw不相同，请一定记得将你的生成方法通过markedHeadingId告诉编辑器
      // 否则编辑器默认的目录定位功能无法正确使用
      const id = raw;

      if (/<a.*>.*<\/a>/.test(text)) {
        return `<h${level} id="${id}">${text.replace(
            /(?<=\<a.*)>(?=.*<\/a>)/,
            ' target="_blank">'
        )}</h${level}>`;
      } else if (text !== raw) {
        return `<h${level} id="${id}">${text}</h${level}>`;
      } else {
        return `<h${level} id="${id}"><a href="#${id}">${raw}</a></h${level}>`;
      }
    }
  },
  setup () {
    const text = ref('')


    return {
      ts1: ref(null),
      ts2: ref(1183135260000),
      range1: ref(null),
      range2: ref(null),
      theme:'dark',
      text:text,
      language: 'my-lang',
      languageUserDefined: {
        'my-lang': {
          toolbarTips: {
            bold: '加粗',
            underline: '下划线',
            italic: '斜体',
            strikeThrough: '删除线',
            title: '标题',
            sub: '下标',
            sup: '上标',
            quote: '引用',
            unorderedList: '无序列表',
            orderedList: '有序列表',
            codeRow: '行内代码',
            code: '块级代码',
            link: '链接',
            image: '图片',
            table: '表格',
            mermaid: 'mermaid图',
            katex: '公式',
            revoke: '后退',
            next: '前进',
            save: '保存',
            prettier: '美化',
            pageFullscreen: '浏览器全屏',
            fullscreen: '屏幕全屏',
            preview: '预览',
            htmlPreview: 'html代码预览',
            catalog: '目录',
            github: '源码地址'
          },
          titleItem: {
            h1: '一级标题',
            h2: '二级标题',
            h3: '三级标题',
            h4: '四级标题',
            h5: '五级标题',
            h6: '六级标题'
          },
          imgTitleItem: {
            upload: '上传图片',
            clip2upload: '裁剪上传'
          },
          linkModalTips: {
            title: '添加',
            descLable: '链接描述：',
            descLablePlaceHolder: '请输入描述...',
            urlLable: '链接地址：',
            UrlLablePlaceHolder: '请输入链接...',
            buttonOK: '确定'
          },
          clipModalTips: {
            title: '裁剪图片上传',
            buttonUpload: '上传'
          },
          copyCode: {
            text: '复制代码',
            tips: '已复制'
          },
          mermaid: {
            flow: '流程图',
            sequence: '时序图',
            gantt: '甘特图',
            class: '类图',
            state: '状态图',
            pie: '饼图',
            relationship: '关系图',
            journey: '旅程图'
          },
          katex: {
            inline: '行内公式',
            block: '块级公式'
          }
        }},


    }

  }
});

</script>

<style>
.md{
  height: calc(100vh - 63px);
}
</style>