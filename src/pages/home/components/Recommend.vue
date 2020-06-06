<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.index">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title" id="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.price}}</p>
          <button class="item-button" id="item-button">查看详情</button>
        </div>
      </li>

    </ul>
  </div>
</template>
<script>
export default{
  name:'HomeRecommend',
  props:{
    list:Array
  },
  data () {
    return {
    }
  }
}
</script>
<style scoped >

  .title{
    line-height: .8rem;
    background-color : #eee;
    text-indent: .2rem;
    margin-top: .2rem;
  }
  .item{
    overflow: hidden;
    display: flex;
    height :1.9rem;
    }
    .item-img
     { width: 1.7rem;
      height :1.7rem;
      padding :.1rem;
      }
      .item-info
        {flex:1;
        padding: .1rem
      }
        

.item-desc{
  line-height :.5rem;
  color :red
}

.item-title{
          line-height : .54rem;
          font-size : .32rem
        }


.item-info .item-button{
 background :#ff9300;
 padding :0 .1rem;
 border-radius : .06rem;
 line-height: .44rem;
 margin-top: .16rem;
 color: #fff;
}




</style>