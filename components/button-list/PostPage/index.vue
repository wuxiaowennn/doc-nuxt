<template>
  <n-upload
      multiple
      directory-dnd
      action="https://www.mocky.io/v2/5e4bafc63100007100d8b70f"
  >
    <n-upload-dragger>
      <div style="margin-bottom: 12px">
        <n-icon size="48" :depth="3" style="font-style:normal;color: #92909c" class="n-icon">
          +
        </n-icon>
      </div>
      <n-text style="font-size: 16px">
        封面上传
      </n-text>
    </n-upload-dragger>
    <div class="font-size">建议尺寸1303*734px</div>
  </n-upload>
</template>

<!--
<script lang="ts">
// import { defineComponent } from 'vue'
// import { ArchiveOutline as ArchiveIcon } from '@vicons/ionicons5'

export default defineComponent({
  components: {
    ArchiveIcon
  }
})
</script>-->

<style>
.n-text{
  color: #92909c
}
.n-icon{
  color: #92909c!important;
}
.n-upload-dragger{
  padding: 10px;
}
.font-size{
  margin-top: 5px;
  color: #92909c
}
.n-upload--dragger-inside{
  display: flex;

}
.n-upload-file--text-type{
  width: 280px;
  /*border: 1px solid red;*/
  text-align: left;
  margin-left: 7px;
}

</style>