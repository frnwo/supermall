<template>
<div id="main-tab-bar">
  <tab-bar>
      <!-- 因为"/home"是固定值，不是变量，所以path前面不用加: -->
      <tab-bar-item path="/home">
        <img class="" slot="item-icon" src="~assets/img/tabbar/home.svg"/>  
        <img class="" slot="item-icon-active" src="~assets/img/tabbar/home_active.svg"/>
        <div slot="item-text">首页</div>
      </tab-bar-item>

      <tab-bar-item path="/category">
        <img class="" slot="item-icon" src="~assets/img/tabbar/category.svg"/>
         <img class="" slot="item-icon-active" src="~assets/img/tabbar/category_active.svg"/>
        <div  slot="item-text">分类</div>
      </tab-bar-item>

      <tab-bar-item path="/cart">
        <img class="" slot="item-icon" src="~assets/img/tabbar/shopcart.svg"/>
         <img class="" slot="item-icon-active" src="~assets/img/tabbar/shopcart_active.svg"/>
        <div  slot="item-text">购物车</div>
      </tab-bar-item>

      <tab-bar-item path="/profile">
        <img class="" slot="item-icon" src="~assets/img/tabbar/profile.svg"/>
         <img class="" slot="item-icon-active" src="~assets/img/tabbar/profile_active.svg"/>
        <div  slot="item-text">我的</div>
      </tab-bar-item>
      
    </tab-bar>
</div>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar';
import TabBarItem from 'components/common/tabbar/TabBarItem';

export default {
  components:{
    TabBar,
    TabBarItem,
  }
}
</script>

<style>

</style>