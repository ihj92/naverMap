<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  
  <div class="town-swiper">
    <swiper
    :slides-per-view="1"
    :space-between="16"
    :centeredSlides="true"
    :pagination="{ clickable: true }"
    :loop="true"
    :looped-slides="card.length"
    :watch-slides-progress="true"
    :loop-fill-group-with-blank="true"
    class="mySwiper">
    <SwiperSlide v-for="(item, index) in card" :key="index">
      <div class="info-card">
        <p>{{ item.title }}</p>
        <p>{{ item.content }}</p>
      </div>
    </SwiperSlide>
  </swiper>
  </div>
</template>

<script lang="ts" setup>
  import { Swiper, SwiperSlide } from 'swiper/vue'

const card = [
  {
  title: '올리브영',
  content : '올리브영에서 함께 일할 직원을 찾습니다.'
  },
  {
  title: '올리브영2',
  content : '올리브영에서 함께 일할 직원을 찾습니다.'
  },
  {
  title: '올리브영33',
  content : '올리브영에서 함께 일할 직원을 찾습니다.'
  },
  {
  title: '4444',
  content : '올리브영에서 함께 일할 직원을 찾습니다.'
  },
]
</script>

<style>
.town-swiper {
  position: fixed;
  bottom: 30px;
  width: 100%;
}
.swiper {
  padding: 0 30px;
}
.info-card {
  position: relative;
  padding: 16px;
  border: 1px solid #e8ecf5;
  border-radius: 12px 40px 12px 12px;
  background-color: #fff;
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
