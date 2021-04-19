<template>
  <div class="Carousel">
    <div v-for="item in imgs" :key="item.src">
      <img :src="item.src">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  props: {
    imgs: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
