<template>
  <div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201406/24/e2a5766e6e81793b2b518a7a08812a4a.jpg_600x330_3a459e19.jpg" />
        <div class="banner-info">
            <div class="banner-title">千岛湖森林氧吧</div>
            <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span> 6 </div>
        </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://img1.qunarzz.com/sight/p0/201406/24/e2a5766e6e81793b2b518a7a08812a4a.jpg_600x330_3a459e19.jpg', 'https://img1.qunarzz.com/sight/p0/1603/e6/e646f4221574cc2a90.water.jpg_600x330_8d179634.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
    .banner
        position:relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img
          width:100%
        .banner-info
          display: flex
          position:absolute
          left: 0
          right: 0
          bottom: 0
          line-height:.6rem
          color: #fff
          background-image: linear-gradient(top, rgba(0, 0, 0
          , 0), rgba(0, 0, 0, 0.8))
          .banner-title
            font-size:.32rem
            flex: 1
            padding: 0 .2rem
          .banner-number
            height:.32rem
            line-height:.32rem
            margin-top: .14rem
            padding: 0 .4rem
            border-radius: .2rem
            background:rgba(0, 0, 0, .8)
            font-size:.24rem
            .banner-icon
              font-size: .24rem
</style>
