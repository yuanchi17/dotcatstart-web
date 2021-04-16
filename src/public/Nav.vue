<template>
  <Disclosure as="nav">
    <!-- <DisclosureButton class="sm:hidden">
      <div v-if="!open" class="w-24 h-24 border-2 border-yellow-900" aria-hidden="true">=</div>
    </DisclosureButton> -->
    <DisclosurePanel static class="flex justify-between p-4 border-b">
      <img class="img-logo my-auto" src="https://dogcatstar.atomcdn.com/2020/07/03/menu_logo.png">
      <div class="hidden sm:flex">
        <Menu v-for="item in navigations" :key="item.name" :item="item"/>
      </div>
      <div class="hidden md:flex md:flex-col lg:flex-row space-x-2">
        <a class=" my-auto py-1 px-4 border bg-yellow-900 rounded-full text-sm text-white text-center transition duration-300 hover:bg-yellow-700"> 登入／註冊</a>
        <a class=" my-auto py-1 px-4 border bg-yellow-900 rounded-full text-sm text-white text-center transition duration-300 hover:bg-yellow-700"> 購物車</a>
      </div>
    </DisclosurePanel>
  </Disclosure>
</template>

<script>
// import { ref } from 'vue'
// import { Disclosure, DisclosureButton, DisclosurePanel, Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import { Disclosure, DisclosurePanel } from '@headlessui/vue'
import Menu from './Menu'

const navigations = [
  {
    name: '關於汪喵',
    en: 'ABOUT US',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: true
  },
  {
    name: '狗狗專區',
    en: 'DOG',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: false
  },
  {
    name: '貓貓專區',
    en: 'CAT',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: false
  },
  {
    name: '活動消息',
    en: 'NEWS',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: false
  },
  {
    name: '汪喵專欄',
    en: 'BLOG',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: false
  },
  {
    name: '合作商店',
    en: 'STORE',
    href: '#',
    info: [{ title: '標題', body: ['內容1', '內容2'] }],
    current: false
  }
]

export default {
  name: 'Nav',
  components: {
    Disclosure,
    DisclosurePanel,
    Menu
    // Menu,
    // MenuButton,
    // MenuItem,
    // MenuItems
  },
  setup () {
    return {
      navigations
    }
  }
}
</script>

<style scoped>
.img-logo {
  max-height: 46px
}
</style>
