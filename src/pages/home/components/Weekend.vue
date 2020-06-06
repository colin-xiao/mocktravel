<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.index">
        <div  class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title" id="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
        imgUrl:'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title:'上海必打卡',
        desc:'中西合璧，现代和传统各有各的精彩'
      },
      {
        id:'0002',
        imgUrl:'http://img1.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg',
        title:'周末亲子爱玩',
        desc:'走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~'
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
  
    .item-img
     { width: 100%;
      
      }
  
        
.item-img-wrapper{
height: 0;
overflow: hidden;
padding-bottom: 33.9%;
}
.item-desc{
  line-height :.4rem;
  color :#ccc
}

.item-title{
          line-height : .54rem;
          font-size : .32rem
        }

        .item-info{
          padding:.1rem
        }






</style>