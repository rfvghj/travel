<template>
  <div class="wrapper">
   <swiper :options="swiperOption">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.url" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      list:[{
      	id:"001",
      	url:'https://img.zcool.cn/community/01a0db579c1d040000018c1beb2f7e.jpg'
      },
      {
      	id:"002",
      	url:'https://img.zcool.cn/community/01a0db579c1d040000018c1beb2f7e.jpg'
      }]
      	
      
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background:#eee
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
