<template>
  <div class="header">
<div class="header-left">
  <div class="iconfont back-icon">&#xe624;</div>
</div>
<div class="header-input">
  <span class="iconfont ">&#xe632;</span>
  输入城市景点游玩主题
  </div>
  <router-link to="/city">
<div class="header-right">{{this.city}}</div> 
  <span class="iconfont down-icon">&#xe64a;</span>
  </router-link>
 </div>
</template>
<script>
export default{
  name:'HomeHeader',
  props:{
    city:String
  }
}
</script>
<style lang='stylus' scoped>
@import '../../../assets/styles/variables.styl';

.header{
  display:flex

  line-height $headerHeight
  background: $bgColor
  color #fff
}

.header-left{
    width : .64rem
    float : left  
}
.header-right{
    width : 1rem
    float : right
    text-align:center
    color:#fff
    }

.header-input{
  flex:1
  background :#fff
  // text-align :center
  margin-top :.12rem
  height :.64rem
  margin-left .2rem
  border-radius :.1rem
  color:#ccc
  line-height :.64rem
  padding-left:.2rem
}

.back-icon{
  text-align :center
  font-size :.4rem
}

.down-icon{
  font-size: .24rem
  margin-left: .2rem
}



</style>