<template>
  <section id="intro">
    <div class="profile">
      <div class="photo_box">
        <p class="photo"></p>
        <p class="introduce">어쩌구 저쩌구 설명</p>
      </div>
      <div class="introduce_txt">
      </div>
    </div>
    <div class="new_article">
      <p>NEW!</p>
      <div class="article_box">
        <p class="article_phpto"></p>
        <p class="article_title">제목이다</p>
        <p class="article_txt">내용 줄임말</p>
        <p class="article">작성 시간</p>
      </div>
    </div>
    <div class="new_pjt">
      <p>PROJECT!</p>
      <swiper
      :slidesPerView="2"
      :centeredSlides="true"
      :spaceBetween="30"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="mySwiper"
      >
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide><swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide><swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide><swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide><swiper-slide>Slide 9</swiper-slide>
      </swiper>
    </div>
  </section>
</template>


<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import { Pagination } from 'swiper/modules';


</script>

<style lang="less" scoped>
#intro {
  width: 100%;
  // display: flex;
  // justify-content: center;
  .profile {
    display: flex;
    justify-content: space-evenly;
    // width: 300px;
    .photo_box {
      border-radius: 20px;
      box-shadow: 5px 5px 5px rgba(189, 189, 189, 0.2);
      width: 300px;
      height: 300px;
      background-color: whitesmoke;
      padding: 20px;
      .photo {
        width: 200px;
        height: 200px;
        border-radius: 100%;
        background-image: url(../assets/logo.svg);
        background-repeat: no-repeat;
        background-position: center;
        margin: 0 auto;
      }
    }
    .introduce_txt {
      width: 800px;
      background-color: whitesmoke;
      box-shadow: 5px 5px 5px rgba(189, 189, 189, 0.2);
      border-radius: 20px;
    }
  }
  .new_article {
    background-color: tan;
    padding: 50px;
    // p {
    //   font-size: 30px;
    // }
    .article_box {
      .article_phpto {
        width: 100%;
        height: 300px;
      }
      width: 20%;
      height: 400px;
      border: 1px solid rgb(235, 235, 235);
    }
  }
  .new_pjt {
    padding: 50px;
    .swiper {
      height: 500px;
      .swiper-slide {
        width: 30%;
      }
      .swiper-slide:hover {
        border: 1px solid black;
      }
    }
  }
}
</style>
