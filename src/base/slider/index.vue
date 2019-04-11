<template>
  <swiper :options="swiperOption">
    <slot></slot>
    <div class="swiper-pagination" v-if="pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
  import {swiper} from 'vue-awesome-swiper';

  export default {
    name: 'MeSlider',
    components: {
      swiper,
    },
    props:{
      direction:{
        type:String,
        default:'horizontal',
        validator(value){
          return [
            'horizontal',
            'vertical'
          ].indexOf(value) > -1;
        },
        interval:{
          type:Number,
          default: 3000,
          validator(value){
            return value >= 0;
          }
        },
        lopp:{
          type:Boolean,
          default:true
        },
        pagination:{
          type:Boolean,
          default:true
        }
      }
    },
    data(){
      return {
        swiperOption:{
          watchOverflow:true, //只有一张图片不滑动
          direction: this.direction,
          autoplay:this.interval ? { // 自动播放
            delay:this.interval,  // 延迟
            disableOnInteraction:false  //交互之后停止轮播
          } : false,
          slidesPerView:1,  // 容器同时显示几张图片
          loop:this.loop,  // 是否开启无缝滚动
          pagination:{
            el:this.pagination ? '.swiper-pagintation' :null,
          }
        }
      }
    }
  }
</script>

<style scoped>

</style>


