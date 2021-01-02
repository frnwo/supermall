<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
    <home-swiper :banners='banners'/>
    <recommend-view :recommends="recommends"/>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import HomeSwiper from "./childComps/HomeSwiper";
import RecommendView from "./childComps/RecommendView";

import { getHomeMultidata } from "network/home";
export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
    RecommendView
  },
  data() {
    return {
      banners:[],
      recommends:[],
    };
  },
  created() {
    // console.log(this); 当前vue组件
    //异步操作
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
      // console.log(this); //箭头函数向外找最近的this，也是当前vue组件
    });
    
  },
};
</script>

<style>
.home-nav {
  background-color: var(--color-tint);
  color: #fff;
}
</style>