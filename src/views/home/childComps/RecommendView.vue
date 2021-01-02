<template>
  <div class="recommend">
    <div v-for="(item,index) in recommends" :key="index">
      <a :href="item.link">
        <img :src="item.image" alt=''/>
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:"RecommendView",
  props:{
    recommends:{
      tyep:Array,
      default(){
        return []
      },
    }
  }
}
</script>

<style>
.recommend{
  display: flex;
  text-align: center;
  font-size: 12px;
  padding: 7px 0 10px;
  border-bottom: 8px solid #eee;
}
.recommend>div{
  flex:1;
  margin: 10px 10px;
}
.recommend img{
  width:100%;
  margin-bottom: 10px;
}

</style>