<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.index">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title" id="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button" id="item-button">查看详情</button>
        </div>
      </li>

    </ul>
  </div>
</template>
<script>
export default{
  name:'HomeRecommend',
  data () {
    return {
      recommendList:[
        {
        id:'0001',
        imgUrl:'http://img1.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg',
        title:'上海迪士尼乐园',
        desc:'全球最大的迪士尼城堡'
      },
      {
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/sight/p0/2005/82/8253605ce47e06eba3.water.jpg_200x200_ad135a76.jpg',
        title:'上海海昌海洋公园',
        desc:'上海最出名地海洋公园'
      },
      {
        id:'0003',
        imgUrl:'http://img1.qunarzz.com/sight/p0/2005/23/23c1b2b13230b966a3.water.jpg_200x200_f3a19805.jpg',
        title:'上海野生动物园',
        desc:'会跳芭蕾的小海狮们～'
      },
      {
        id:'0004',
        imgUrl:'http://img1.qunarzz.com/sight/p0/2005/9e/9e643f96c84b5c2ea3.water.jpg_200x200_2a3eef5b.jpg',
        title:'上海欢乐谷',
        desc:'敢上1200米长的木质过山车吗？'
      }
      ]
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
  line-height :.4rem;
  color :#ccc
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