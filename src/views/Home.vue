<template>
  <div class="home">
    <Carousel :imgs="carouselImgs"/>
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 m-8">
      <a :href="group.href" target="_blank" v-for="group in groupImgs" :key="group.src" class="w-4/5 md:w-auto lg:w-4/5 mx-auto my-auto ">
        <img :src="group.src" class="transform hover:scale-125 transition duration-500">
      </a>
    </div>
    <div class="flex flex-col">
      <img src="https://dogcatstar.atomcdn.com/2020/07/03/955206/title_popular-1.png" class="h-auto sm:h-16 mx-auto">
      <div class="grid grid-cols sm:grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4 mx-4 my-8 sm:mx-16">
        <Card :item="item" v-for="item in hotItems" :key="item.title"/>
      </div>
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
import Carousel from '@/components/Carousel.vue'

const carouselImgs = [
  // { src: 'https://dogcatstar.atomcdn.com/2020/07/03/955206/oldgodcan_SC2-2.jpg', href: '/' },
  // { src: 'https://dogcatstar.atomcdn.com/2020/07/03/955206/bondline_SC-1.jpg', href: '/' },
  { src: 'https://dogcatstar.atomcdn.com/2020/07/03/955206/oldgodcan_SC2.jpg', href: '/' }
]

const groupImgs = [
  { src: 'https://dogcatstar.atomcdn.com/2020/07/05/1078537/btnA_01_hover@2x.jpg', href: '/' },
  { src: 'https://dogcatstar.atomcdn.com/2020/07/05/1078537/btnA_02_hover@2x.jpg', href: '/' },
  { src: 'https://dogcatstar.atomcdn.com/2020/07/05/1078537/btnA_03_hover@2x.jpg', href: '/' },
  { src: 'https://dogcatstar.atomcdn.com/2020/07/05/1078537/btnA_04_hover@2x.jpg', href: '/' }
]

const hotItems = [
  {
    title: '犬用 95% 鮮肉無膠主食罐',
    price: 'NT$46 - NT$1.176',
    imgs: [
      'https://dogcatstar.atomcdn.com/2017/07/06/42495/dogcan-P1-510x510.jpg',
      'https://dogcatstar.atomcdn.com/2017/07/06/42495/dogcan-P2-510x510.jpg'
    ]
  },
  {
    title: '貓用 98 %鮮肉無膠主食罐',
    price: 'NT$46 - NT$1.176',
    imgs: [
      'https://dogcatstar.atomcdn.com/2017/03/30/32602/fantasticcat-01P-2-510x510.jpg',
      'https://dogcatstar.atomcdn.com/2017/03/30/32602/fantasticcat-換包裝-510x510.jpg'
    ]
  },
  {
    title: '汪喵排毛粉',
    price: 'NT$46 - NT$1.176',
    imgs: [
      'https://dogcatstar.atomcdn.com/2017/03/16/31215/hairball_relief_digestive_aid-01P-510x510.jpg',
      'https://dogcatstar.atomcdn.com/2017/03/16/31215/digestive-aid_P2-510x510.jpg'
    ]
  },
  {
    title: '汪喵星球 100% PURE 純離胺酸',
    price: 'NT$46 - NT$1.176',
    imgs: [
      'https://dogcatstar.atomcdn.com/2017/11/01/56709/l-lysine-01P-510x510.jpg',
      'https://dogcatstar.atomcdn.com/2017/11/01/56709/l-lysine-P02-510x510.jpg']
  },
  {
    title: '汪喵沙西米｜狗狗生肉餐（主食）',
    price: 'NT$46 - NT$1.176',
    imgs: [
      'https://dogcatstar.atomcdn.com/2015/12/10/7211/doghpprawfood-P2-510x510.jpg',
      'https://dogcatstar.atomcdn.com/2015/12/10/7222/doghpprawfood-01P-510x326.jpg']
  }
]

export default {
  name: 'Home',
  components: {
    Card,
    Carousel
  },
  setup () {
    return {
      carouselImgs,
      groupImgs,
      hotItems
    }
  }
}
</script>
