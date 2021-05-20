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
      <div class="grid grid-cols sm:grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4 mx-4 sm:mx-16 my-8">
        <Card :item="item" v-for="item in hotItems" :key="item.title"/>
      </div>
    </div>
    <div class="flex flex-col">
      <img src="https://dogcatstar.atomcdn.com/2020/07/03/955206/title_share-1.png" class="h-auto sm:h-16 mx-auto">
      <div class="grid grid-cols md:grid-cols-2 gap-4 mx-4 sm:mx-16 my-8">
        <CardShare :item="item" v-for="item in shareItems" :key="item.name"/>
      </div>
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
import CardShare from '@/components/CardShare.vue'
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

const shareItems = [
  {
    name: '扭扭',
    img: 'https://i.imgur.com/yCC8VdH.png',
    food: '挑嘴貓無膠主食罐',
    intro: '自從在寵物展買過汪喵挑嘴罐後，扭扭一試成主顧，終於！終結了媽媽找不到適合又安心的罐罐噩夢！'
  },
  {
    name: '來福',
    img: 'https://i.imgur.com/yCC8VdH.png',
    food: '95% 鮮肉無膠主食罐',
    intro: '來福食量大很難全濕食，但又怕營養不夠，所以偶爾會在來福的飼料裡面拌汪喵罐罐，營養均衡，長得更帥了！'
  },
  {
    name: '麻糬',
    img: 'https://i.imgur.com/yCC8VdH.png',
    food: '冷凍乾燥生食餐',
    intro: '為了讓麻糬轉吃生食而先選擇凍乾，結果嗜口性超好，不攝取澱粉飼料後，麻糬體態變得精實、大便比較不臭也不再容易軟便！'
  },
  {
    name: 'QQ',
    img: 'https://i.imgur.com/yCC8VdH.png',
    food: '益生菌',
    intro: '臘腸很容易過敏濕疹，嘗試了益生菌搭配生食之後，皮膚眞的越來越好了，天氣潮濕都不會再犯濕疹了！'
  }
]

export default {
  name: 'Home',
  components: {
    Card,
    CardShare,
    Carousel
  },
  setup () {
    return {
      carouselImgs,
      groupImgs,
      hotItems,
      shareItems
    }
  }
}
</script>
