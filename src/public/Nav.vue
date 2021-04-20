<template>
  <Disclosure as="div" class="flex justify-between p-4 border-b">
    <DisclosureButton class="md:hidden focus:outline-none">
      <MenuIcon class="h-6 w-6 text-yellow-900" aria-hidden="true" />
    </DisclosureButton>
    <a href="/" target="_blank" class="img-logo my-auto mx-auto md:mx-0"><img src="https://dogcatstar.atomcdn.com/2020/07/03/menu_logo.png"></a>
    <DisclosurePanel class="flex flex-col md:hidden absolute top-20 inset-x-0 z-10 py-2 bg-white border-2 border-yellow-900 rounded">
      <a href="/" target="_blank" v-for="item in navigations" :key="item.name" class=" w-24 my-auto mx-auto px-4 py-2 text-yellow-900  border-b-2 border-yellow-900 border-opacity-0 transition duration-300 hover:border-opacity-50 focus:outline-none">
        {{ item.name }}
        <p class="text-xs text-yellow-500"> {{ item.en }}</p>
      </a>
    </DisclosurePanel>

    <div class="hidden md:flex">
      <Menu v-for="item in navigations" :key="item.name" :item="item"/>
      <div class="hidden lg:flex space-x-2">
        <a href="/" target="_blank" class=" my-auto py-1 px-4 text-sm text-center yellow-rounded-full"> 登入／註冊</a>
        <a href="/" target="_blank" class=" my-auto py-1 px-4 text-sm text-center yellow-rounded-full"> 購物車</a>
      </div>
      <div class="lg:hidden flex space-x-2">
        <a href="/" target="_blank" class="h-10 w-10 my-auto p-2 yellow-rounded-full"><UserIcon/></a>
        <a href="/" target="_blank" class="h-10 w-10 my-auto p-2 yellow-rounded-full"><ShoppingCartIcon/></a>
      </div>
    </div>
  </Disclosure>
</template>

<script>
import { Disclosure, DisclosurePanel, DisclosureButton } from '@headlessui/vue'
import { MenuIcon, UserIcon, ShoppingCartIcon } from '@heroicons/vue/outline'
import Menu from './Menu'

const navigations = [
  {
    name: '關於汪喵',
    en: 'ABOUT US',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      }],
    current: true
  },
  {
    name: '狗狗專區',
    en: 'DOG',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      },
      {
        title: '標題2',
        body: [
          { title: '內容2-1', href: '/' },
          { title: '內容2-2', href: '/' }
        ]
      }
    ],
    current: false
  },
  {
    name: '貓貓專區',
    en: 'CAT',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      }],
    current: false
  },
  {
    name: '活動消息',
    en: 'NEWS',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      }],
    current: false
  },
  {
    name: '汪喵專欄',
    en: 'BLOG',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      }],
    current: false
  },
  {
    name: '合作商店',
    en: 'STORE',
    href: '#',
    info: [
      {
        title: '標題',
        body: [
          { title: '內容1', href: '/' },
          { title: '內容2', href: '/' }
        ]
      }],
    current: false
  }
]

export default {
  name: 'Nav',
  components: {
    Disclosure,
    DisclosureButton,
    DisclosurePanel,
    Menu,
    MenuIcon,
    ShoppingCartIcon,
    UserIcon
  },
  setup () {
    return {
      navigations
    }
  }
}
</script>

<style scoped>
@import './../assets/tailwind.css';
.img-logo {
  max-height: 46px
}

</style>
