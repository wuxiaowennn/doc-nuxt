<template>
<div>
  <div class="box w-full">
     <div class="box-son w-full">
       <div class="logo-box w-full">
         <div class="logo"></div>
       </div>
       <div class="search">
         <input type="text" class="search-box" onfocus="if(value=='搜索'){value=''}" onblur="if(value==''){value='搜索'}" value="搜索">
       </div>
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
.box{
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  height: 214px;
  /*border: 1px solid red;*/
  background: #17181a;

}
.box-son{
  display: flex;
  justify-content: center;
  height: 136px;
  color: white;
  /*border: 1px solid seagreen;*/
  flex-wrap: wrap;

}
.logo{
  width: 160px;
  height: 36px;
  /*margin-top: 93px;*/
  /*background: red;*/
  background: url(https://weread-1258476243.file.myqcloud.com/web/wrwebnjlogic/image/search_header_logo.02fc8d01.png
  ) no-repeat;
}
.logo-box{
  flex-wrap: wrap;
  height: 36px;
  display: flex;
  justify-content: center;
  /*border: 1px solid #42b983;*/


}
.search{
  width: 840px;
  height: 52px;
  justify-content: center;
  align-items: center;

}
.n-input-wrapper{
  width: 840px;
  height: 52px;
}

.search-box{
  width: 840px;
  height: 52px;
  padding-left:40px;
  border-radius: 24px;
  background: #2d2e30;
  border: 0px solid rgba(0,0,0,0);
  color: #818387;
  outline: none;
}

</style>