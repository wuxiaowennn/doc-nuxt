<template>
  <div>
  <n-space>
    <n-popover
        :show="showPopover"
        placement="bottom"
        trigger="manual"
    >
      <template #trigger>
        <n-button @click="showPopover = !showPopover" class="button1 w-full">
          发布
        </n-button>
      </template>
      <div class="h-[85vh]" style="width: 560px">
          <Button-ListTags></Button-ListTags>
          <Button-ListClass></Button-ListClass>
      </div>

    </n-popover>
  </n-space>
  </div>
</template>

<script setup>

let showPopover =  ref(false);
</script>

<style scoped>
.button1{
  border:0;
  background: #1d7dfa;
  color: white;
}
.button1:hover{
  background: #388eff!important;
  color: white!important;
}
.n-button:not(.n-button--disabled):hover {
  background-color: #388eff!important;
  color: white!important;
}
.n-button:not(.n-button--disabled):focus {
  background-color: #388eff!important;
  color: white!important;
}
.n-button .n-base-wave {
  animation: none;

}
.n-button{
  width:62px;
  height:32px;
}
.v-binder-follower-content{
  transform: translateX(1500px) translateY(63px) translateX(-100%)!important;
  --v-offset-left: 74px!important;
}

.n-popover--show-arrow {
  padding: 0!important;
}
.pl-9 {
  padding-left: 0.25rem;
}
</style>