<template>
  <div id="appxx">
    <router-view/>
   <main-tab-bar></main-tab-bar>
  </div>
</template>

<script>

import MainTabBar from 'components/content/mainTabBar/MainTabBar';
export default {
  name: 'App',
  components: {
    MainTabBar,
  }
}
</script>

<style>
/**引入base.css */
 @import "assets/css/base.css";
</style>
