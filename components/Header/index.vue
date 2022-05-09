<template>
<div>
  <div class="header">
    <div class="header-son xs:invisible sm:visible">
      <ul class="header-ul">
        <li class="line">传书到手机</li>
        <li  class="line">墨水屏版本</li>
        <li  class="line">手机版</li>
        <li  class="line">微信听书</li>
        <li>登录</li>
      </ul>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style scoped>
.header{
  display: flex;
  justify-content: center;
  width: 100%;
  height: 72px;
  background: #17181a;
  /*border: 1px solid red;*/

}
.header-son{
  display: flex;
  align-items: center;
  justify-content: flex-end;
  width: 1332px;
  height: 72px;
  /*border:1px solid blue;*/
}
.header-ul{
  display: flex;

}
.line::after{
  content: '|';
  padding-left:10px;
  width: 1px;
  color: #5c5d5e;


}
.header-ul>li{
  margin-left:12px ;
  color: #b9b9ba;
}
.header-ul>li:hover{
  color: #ffffff;
}
</style>