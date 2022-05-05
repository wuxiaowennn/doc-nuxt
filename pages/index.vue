<template>
<div>
     <div class='text-4xl w-20 h-20 mx-auto'>21341231</div>
     <n-space>
        <n-button type="error">按钮</n-button>
         <n-button type="tertiary">
      Tertiary
    </n-button>
     </n-space>
    <n-space vertical>
    <n-date-picker v-model:value="ts1" type="date" :actions="['now']" />
    <n-date-picker v-model:value="ts2" type="datetime" :actions="['now']" />
    <n-date-picker v-model:value="range1" type="daterange" :actions="null" />
    <n-date-picker
      v-model:value="range2"
      type="datetimerange"
      :actions="['clear']"
    />
  </n-space>
  <n-carousel>
    <img
      class="carousel-img"
      src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg"
    >
    <img
      class="carousel-img"
      src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
    >
    <img
      class="carousel-img"
      src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel3.jpeg"
    >
    <img
      class="carousel-img"
      src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel4.jpeg"
    >
  </n-carousel>
</div>
 
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup () {
    return {
      ts1: ref(null),
      ts2: ref(1183135260000),
      range1: ref(null),
      range2: ref(null)
    }
  }
})
</script>

<style>
.carousel-img {
  width: 100%;
  height: 240px;
  object-fit: cover;
}
</style>