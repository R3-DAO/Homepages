<template>
  <swiper id="swiperBox" v-bind:options="swiperOption">
    <swiper-slide class="swiper-slide slide-one">
      <a href="mailto:cmark2022@outlook.com"></a>
    </swiper-slide>
    <swiper-slide class="swiper-slide slide-two"></swiper-slide>
    <swiper-slide class="swiper-slide slide-three"></swiper-slide>
    <swiper-slide class="swiper-slide slide-four"></swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>
 
<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "Home",
  components: {
    swiper,
    swiperSlide,
  },
  data() {
    return {
      swiperOption: {
        notNextTick: true,
        direction: "vertical",
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        grabCursor: true,
        setWrapperSize: true,
        autoHeight: true,
        slidesPerView: 1,
        mousewheel: true,
        mousewheelControl: true,
        height: window.innerHeight - 100,
        resistanceRatio: 0,
        observeParents: true,
      },
    };
  },
  created() {},
  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    },
  },
  mounted() {},
};
</script>
 
<style lang="scss" scoped>
.slide-one {
  background: url(../assets/imgs/R3-001.jpeg) no-repeat;
  background-size: contain;
  a {
    position: absolute;
    bottom: 10px;
    right: 50px;
    color: #fff;
    font-size: 20px;
    width: 300px;
    height: 50px;
  }
}
.slide-two {
  background: url(../assets/imgs/R3-002.jpeg) no-repeat;
  background-size: contain;
}
.slide-three {
  background: url(../assets/imgs/R3-003.jpeg) no-repeat;
  background-size: contain;
}
.slide-four {
  background: url(../assets/imgs/R3-004.jpeg) no-repeat;
  background-size: contain;
}
</style>