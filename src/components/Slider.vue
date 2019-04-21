<template>
  <div class="slider">
    <swiper :options="swiperOption">
      <swiper-slide class="slide-1">
        <div class="slide">
          <img
            src="https://images.pexels.com/photos/1329061/pexels-photo-1329061.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=1000"
            alt
          >
        </div>
      </swiper-slide>
      <swiper-slide class="slide-2">
        <div class="slide">
          <img
            src="https://images.pexels.com/photos/585419/pexels-photo-585419.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=1000"
            alt
          >
        </div>
      </swiper-slide>
      <swiper-slide class="slide-1">
        <div class="slide">
          <img
            src="https://images.pexels.com/photos/1329061/pexels-photo-1329061.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=1000"
            alt
          >
        </div>
      </swiper-slide>
      <swiper-slide class="slide-2">
        <div class="slide">
          <img
            src="https://images.pexels.com/photos/585419/pexels-photo-585419.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=1000"
            alt
          >
        </div>
      </swiper-slide>
      <div class="swiper-pagination swiper-pagination-white" slot="pagination"></div>
      <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
      <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        spaceBetween: 30,
        effect: "fade",
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        loop: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  }
};
</script>

<style scoped>
.slide {
  /* max-width: 1600px; */
  width: 100%;
  height: calc(100vh - 70px);
  position: relative;
}
.slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.slider .swiper-container {
    /* z-index: -1 !important; */
}
/* .swiper-slide {
  background-position: center;
  background-size: cover;
}
.swiper-slide.slide-1 {
  background-image: url("");
}
.swiper-slide.slide-2 {
  background-image: url("");
} */
</style>
