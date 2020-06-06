<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.index">
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
  }
  
    .item-img
     { width: 100%;
      
      }
  
        
.item-img-wrapper{
height: 0;
overflow: hidden;
padding-bottom: 37.09%;
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