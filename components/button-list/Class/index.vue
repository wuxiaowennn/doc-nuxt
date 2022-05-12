<template>
<div>
  <div class="w-full h-[65vh] c-box pl-9 pt-5">
    <table>
      <tr class="box-right" style="display: flex;justify-content: flex-end">
        <td style="display: flex;justify-content: end;width: 90px"><i style="align-items: center;color: red;margin-right: 10px;text-align: right;" class="text-lg mr-0.5 box-center">*</i>分类：</td>
         <td><ButtonListSort></ButtonListSort></td>
      </tr>
      <tr class=" box-right" style="display: flex;align-items: center;margin-top: 13px">
        <td style="display: flex;align-items: center;width: 91px"><i style=" display: flex;align-items: center;color: red;margin-right: 10px;padding-top: 10px" class="text-lg box-center">*</i>添加标签：</td>
        <td  style="display: flex;align-items: center;">
          <ButtonListForm></ButtonListForm>
        </td>
      </tr>
      <tr class=" box-right" style="display: flex;margin-top: 13px">
        <td style="width: 90px">文章封面：</td>
        <td> <ButtonListPostPage></ButtonListPostPage> </td>
      </tr>

      <tr class="h-24" style="display: flex;margin-top: 24px">
        <td style="width: 90px" class="box-right">编辑摘要：</td>
        <td><ButtonListAbs></ButtonListAbs></td>
      </tr>
    </table>

  </div>
</div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style scoped>
.c-box{
  /*border:1px solid red;*/
}

.box-right{
  text-align: right;
}
.box-center{
  /*border: 1px  solid royalblue;*/

}
</style>