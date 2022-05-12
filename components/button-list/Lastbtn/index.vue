<template>
<div class=" w-full h-16 head">
<button class="btn1" style="margin-right: 20px;">取消</button>
  <button class="btn2">确定并发送</button>
</div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style scoped>
.head{
  margin-top: 10px;
  display: flex;
  border-top: 1px solid #cccccc;
  align-items: center;
  justify-content: flex-end;
  padding-right:28px
}
.head>button{
  width: 90px;
  height: 32px;
  /*border: 1px solid red;*/
}
.btn1{
  border: 1px solid #1e80ff;
  border-radius: 3px;
}
.btn2{
  background: #1e80ff;
  color: white;
  border-radius: 3px;
}
</style>