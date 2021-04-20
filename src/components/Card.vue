<template>
<div class="flex sm:flex-col border rounded shadow">
  <div class="w-40 sm:w-full my-auto overflow-hidden">
    <img :src="item.imgs[0]" alt="示意圖" class="w-full transform hover:scale-125 transition duration-500">
  </div>
  <div class="flex flex-col p-2 mx-auto w-full">
    <div class="flex flex-col text-left sm:text-center sm:h-28 h-auto space-y-2">
      <p class="text-md font-semibold">{{ item.title }}</p>
      <p class="text-gray-500 text-sm">{{ item.price }}</p>
    </div>
    <div class="mt-4 sm:mt-0 mb-2 ml-auto sm:mx-auto">
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
