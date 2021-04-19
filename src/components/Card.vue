<template>
<div class="flex sm:flex-col border rounded">
  <!-- TODO: 手機板大小 -->
  <img :src="item.imgs[0]" alt="示意圖" class="w-40 sm:w-auto ">
  <div class="flex flex-col p-2 mx-auto justify-between w-full">
    <div class="flex flex-col h-28 text-left sm:text-center">
      <p class="text-lg font-semibold">{{ item.title }}</p>
      <p class="pt-2 text-gray-500 text-sm">{{ item.price }}</p>
    </div>
    <div class="mb-2 ml-auto sm:mx-auto">
      <a href="/" class="p-2 yellow-rounded">選擇規格</a>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Carousel',
  props: {
    item: Object
  }
}
</script>

<style>
@import './../assets/tailwind.css';
</style>
