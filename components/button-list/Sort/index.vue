<template>
  <div class=" w-[450px] overflow-hidden">
    <ul  class="overflow-hidden ">
      <li class="border w-20 h-9 float-left text-center mr-8 leading-9 mb-3 box-ul-li" :class="{'active':items.id == isActive }" v-for="items in data" :key="items.id" @click="show(items.id)">{{items.name}}</li>
    </ul>
  </div>

</template>

<script setup>
  let isActive = ref('')
  const show = (items)=>{
    isActive.value = items
  }

  const data = reactive([
    {id:1,name:'后端'},
    {id:2,name:'前端'},
    {id:3,name:'Android'},
    {id:4,name:'iOS'},
    {id:5,name:'开发工具'},
    {id:6,name:'代码人生'},
    {id:7,name:'阅读'},
    {id:8,name:'人工智能'}
  ])
</script>

<style scoped>

.box-ul-li{
  border-radius: 2px;
  background: #f4f5f5;
  color: #92909c;
   /*margin: 0.3rem;*/

}
.box-ul-li:hover{
  background: #e5e6eb;
  cursor: pointer;

}
.active{
  background:#e8f3ff!important;
  color:#1d90fb!important;
}
</style>