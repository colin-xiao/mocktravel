<template>
  <div>
    <detail-banner :sightName="sightName" :bannerImg="bannerImg" :galleryImgs="galleryImgs"/>
      <detail-header />
      <detail-list :list='list'/>
    <div class="content"></div>
  </div>
</template>
<script>
import DetailBanner from './components/Banner';
import DetailHeader from './components/Header';
import DetailList from './components/List'; 

import axios from 'axios';

export default{
  name:"Detail",
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      sightName:'',
      bannerImg:'',
      galleryImgs:'',
      categoryList:'',
      list:[]
    }
  },
  methods: {
    getDetailInfo(){
      axios.get('api/detail.json?id=',{
        params:{
          id:this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc(res){
      res = res.data;
      if(res.ret && res.data){
        const data = res.data
        this.sightName = data.sightName   
        this.bannerImg = data.bannerImg     
        this.galleryImgs = data.galleryImgs
        this.list = data.categoryList
      }
    }
  },
  mounted () {
    this.getDetailInfo();
  }
}
</script>
<style scoped lang='stylus'>
  .content  
    height 50rem
</style>