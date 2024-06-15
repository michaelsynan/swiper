<template>
  <div>
    <Swiper
      :pagination="true"
      :modules="[SwiperAutoplay, SwiperEffectCreative, Pagination]"
      :slides-per-view="1"
      :loop="true"
      :effect="'creative'"
      :autoplay="{
        delay: 1000,
        disableOnInteraction: false,
      }"
      :creative-effect="{
        prev: {
          shadow: false,
          translate: ['-20%', 0, -1],
        },
        next: {
          translate: ['100%', 0, 0],
        },
      }"
    >
      <SwiperSlide style="background-color: red;">
        <strong>Slide 1</strong>
      </SwiperSlide>
      <SwiperSlide style="background-color: blue;">
        <strong>Slide 2</strong>
      </SwiperSlide>
      <SwiperSlide style="background-color: green;">
        <strong>Slide 3</strong>
      </SwiperSlide>
      <SwiperSlide style="background-color: yellow;">
        <strong>Slide 4</strong>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<style scoped>
.swiper {
  width: 500px;
  height: 300px;
  border-radius: 10px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>

<script setup>
import { Pagination } from 'swiper/modules';
</script>
