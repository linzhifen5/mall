<template>
  <div class="home">
    <!-- 头部 -->
    <header class="g-header-container">
        <home-header></home-header>
    </header>
    <!-- 内容 -->
    <div>
        <home-slide>
          
        </home-slide>
    </div>
    <!-- 回到首页 -->
    <div class="g-backtop-container"></div>
    <router-view></router-view>
  </div>
</template>

<script>
import HomeHeader from "./header";
import HomeSlide from "./slide";

export default {
  name: "Home",
  components:{
      HomeHeader,
      HomeSlide
  }
};
</script>



