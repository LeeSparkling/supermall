<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物首页</div>
    </nav-bar>
    <HomeSwiper :banners="banners"/>
    <recommend-view :recommends="recommends"/>
  </div>
</template>

<script>
  import NavBar from "../../components/common/navbar/NavBar"
  import HomeSwiper from './childComps/HomeSwiper'
  import RecommendView from './childComps/RecommendView'

  import {getHomeMultidata} from "../../network/home";

  export default {
    name: "Home",
    components:{
      NavBar,
      HomeSwiper,
      RecommendView
    },
    data(){
      //垃圾回收
      return {
        banners:[],
        recommends:[]
      }
    },

    created() {
      //1.请求多个数据
      getHomeMultidata().then(res=>{
        //数据 解构
        this.banners=res.data.banner.list;
        this.recommends=res.data.recommend.list;
      })
    }
  }
</script>

<style scoped>
  .home-nav{
    background-color: #ff8198;
    color: #fff;
  }
</style>
