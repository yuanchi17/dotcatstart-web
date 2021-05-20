<template>
<div class="flex border rounded p-3 space-x-2 shadow">
  <div class="flex">
    <img :src="item.img" alt="寵物的大頭照" class="rounded my-auto">
  </div>
  <div class="flex flex-col">
    <div class="flex flex-col space-x-2 pb-1 border-b">
      <p class="text-2xl font-semibold text-yellow-900">{{ item.food }}</p>
      <p class="text-base text-gray-500">毛小孩：{{ item.name }}</p>
    </div>
    <p class="text-left p-2 text-gray-500">{{ item.intro }}</p>
  </div>
</div>
</template>

<script>
export default {
  name: 'CardShare',
  props: {
    item: Object
  }
}
</script>

<style>
@import './../assets/tailwind.css';
</style>
