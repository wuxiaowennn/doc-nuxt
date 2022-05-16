<template>
<div>
  <div class="title-box w-full">
        <div class="title">
          <input type="text" value="输入文章标题..." class="input" onfocus="if(value=='输入文章标题...'){value=''}" onblur="if(value==''){value='输入文章标题...'}">
        </div>
        <div class="publish">
          <div>保存成功</div>
          <div>
            <button class="draft">草稿箱</button>
          </div>
          <div class="release-btn"><a> <Button-1></Button-1> </a></div>

          <div>
            <div class="login-header">
                头像
            </div>
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
.title-box{
  display: flex;
  align-items: center;
  height: 64px;
  /*border: 1px solid red;*/
}
.title{
  display: flex;
  /*border: 1px solid gold;*/
  flex: 7;
  height: 63px;
}
.input{
  flex: 1;
  outline: none;
  color: #86909c;
  font-size: 24px;
  padding-left: 40px;
}
.publish{
  /*border: 1px solid violet;*/
  flex: 2;
  height: 63px;
}
.publish{
  display: flex;
  justify-content: space-around;


}
.publish>div{
  height: 63px;
  line-height: 63px;
  /*border:1px solid red;*/
  flex: 1;
  text-align: center;
}
.publish>div:nth-child(1){
  font-size: 14px;
  color: #c9cdd4;
}
.draft{
  border:1px solid #1d7dfa;
  width: 76px;
  height: 32px;
  line-height: 30px;
  font-size: 14px;
  color: #1d7dfa;
}
.publish>div:nth-child(2){
  padding: 0 8px;
}
.publish>div:nth-child(3)>button{
  background: #1d7dfa;
  color: white;
  width: 62px;
  height: 32px;
  border-radius: 2px;
  line-height: 32px;
  font-size: 14px;
}

.publish>div:nth-child(4){
  display: flex;
  justify-content: center;
  align-items: center;
}
.login-header{
  width: 2.667rem;
  height: 2.66rem;
  line-height: 2.66rem;
  border-radius: 50%;
  background: red;
}
.login-header:hover{
  cursor: pointer;
}

</style>