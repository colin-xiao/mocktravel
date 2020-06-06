<template>
  <div class="icons">
    <swiper ref="mySwiper"  :options="swiperOptions">
      <swiper-slide v-for="page of pages" :key="page.index">
        <div class="icon"
        v-for='item of page'
        :key="item.index"
        >
          <div class="icon-img">
          <img class="icon-img-content" :src='item.imgUrl'>
          </div>
          <p class="icon-desc">{{item.title}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>
</template>
<script>
export default{
  name:'HomeIcons',
  props:{
    list:Array
  },
  data () {
    return {
     swiperOptions:{
        autoplay:true,
        loop:true
      }
    }
  },
  computed: {
    pages(){
      const pages=[]
      this.list.forEach((item,index)=>{
        const page = Math.floor(index/8)
        if(!pages[page]){
          pages[page] =[]
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style scoped lang="stylus">
@import '../../../assets/styles/variables.styl';
@import '../../../assets/styles/mixins.styl';


.icons >>> .swiper-container
  height 0;
  padding-bottom 50%
  


 .icons
    height:0
    width 100%
    padding-bottom 50%
    overflow hidden
    .icon
      position relative
      overflow hidden
      float left
      height 0
      width 25%
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        box-sizing border-box
        padding .1rem
        left 0
        right 0
        bottom .44rem
        .icon-img-content
          display block
          margin 0 auto
          height 100%
    .icon-desc
      position absolute
      bottom 0
      line-height .44rem
      height .44rem
      left 0
      right 0
      color $darkTextColor
      text-align center
      ellipsis()

.icons{
  margin-top: .1rem
}
</style>