<template>
  <me-navbar class="header" title="">
    <i class="iconfont icon-scan" slot="left"></i>
    <i slot="center">搜索框</i>
    <i class="iconfont icon-msg" slot="right"></i>
  </me-navbar>
</template>

<script>
import MeNavbar from "base/navbar";
export default {
  name: "HomeHeader",
  components: {
    MeNavbar
  }
};
</script>

<style lang="scss" scoped>
@import "~assets/scss/mixins";

.header {
  &.mine-navbar {
    // background-color: $header-bgc-translucent;
    background-color: rgba(222, 24, 27, 0.1);
  }

  .iconfont {
    color: $icon-color-default;
    font-size: $icon-font-size;
  }
}
</style>


