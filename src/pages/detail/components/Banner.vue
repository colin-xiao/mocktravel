<template>
  <div class="banner">
    <img  class="banner-img" src="http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_600x330_feb1c240.jpg" alt="">
    <div class="banner-info">
      <div class="banner-title">上海迪士尼乐园</div>
      <div class="banner-number"><span class="iconfont banner-icon">&#xe635;104</span>
</div>
    </div>
  </div>
</template>
<script>
export default{
  name:"DetailBanner"
}
</script>
<style scoped lang='stylus'>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    color #fff
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      background-image liner-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex 1
        font-size .4rem
        padding 0 .2rem
      .banner-number
        margin-top .2rem
        padding 0 .4rem
        line-height .32rem
        height .32rem
        border-radius .2rem
        background rgba(0,0,0,.8) 
        font-size .24rem
        .banner-icon
          font-size .24rem




</style>