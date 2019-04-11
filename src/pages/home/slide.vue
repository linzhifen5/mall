<template>
    <me-slider
      :direction="direction"
      :loop="loop"
      :interval="interval"
      :pagination="pagination"
    >

      <swiper-slide
        v-for="(item) in sliders">
        <a :href="item.linkUrl" class="slider-link">
          <img :src="item.picUrl" alt="" class="slider-img">
        </a>
      </swiper-slide>
    </me-slider>
</template>

<script>
import MeSlider from 'base/slider';
import { swiperSlide } from 'vue-awesome-swiper';

export default {
    name:'HomeSlider',
    components: {
      MeSlider,
      swiperSlide
    },
  data(){
      return {
        direction:'vertical',
        loop:false,
        interval:0,
        pagination:false,
        sliders:[
          {
            'linkUrl':'https://www.imooc.com',
            'picUrl':require('./1.jpg')
          },
          {
            'linkUrl':'https://www.imooc.com',
            'picUrl':require('./2.jpg')
          },
          {
            'linkUrl':'https://www.imooc.com',
            'picUrl':require('./3.jpg')
          },
        ]
      }
  }
}
</script>

<style scoped>

</style>



