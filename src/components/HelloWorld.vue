<template>

  <div class="block wrapper">
    <div class="main-box relative w-full">
      <div class="animation-container relative">
        <div class="overlay img-uzb absolute top-0 right-0 w-full h-full flex-col flex items-center justify-center">
          <img class="absolute" src="../assets/uzbekistans.png" alt="">
        </div>
        <video
            ref="video"
            autoplay
            muted
            loop
            playsinline
            class="w-full h-full video"
            src="../assets/uzbekistans.mp4">
        </video>
      </div>
      <div class="absolute heightDiv top-[24%] right-[16%] w-full h-full" style="width: 718px; height: 360px">
        <div class="container relative h-full main-img z-[999]">
          <img class="img cursor-pointer img1 absolute top-[64px] left-[-90px] z-[999]" src="../assets/5.png" alt="">
          <img class="img cursor-pointer img2 absolute top-[-20px] left-[164px] z-[999]" src="../assets/2.png" alt="">
          <img class="img cursor-pointer img3 absolute top-[-20px] right-[0px] z-[999]"
               src="../assets/3.png" alt="">
          <img class="img cursor-pointer img4 absolute top-[114px] right-[-94px] z-[999]"
               src="../assets/4.png" alt="">
          <img class="img cursor-pointer img5 absolute bottom-[40px] right-[-93px] z-[999]"
               src="../assets/1.png" alt="">
          <img class="img cursor-pointer img6 absolute bottom-[-120px] right-[20px] z-[999]"
               src="../assets/6.png" alt="">
          <img class="img cursor-pointer img7 absolute bottom-[-120px] right-[160px] z-[999]"
               src="../assets/7.png" alt="">
          <img class="img cursor-pointer img8 absolute bottom-[-120px] left-[90px] z-[999]"
               src="../assets/8.png" alt="">
          <img class="img cursor-pointer img9 absolute bottom-[20px] left-[-100px] z-[999]"
               src="../assets/9.png" alt="">
        </div>
      </div>

    </div>
  </div>


</template>

<script setup lang="ts">
import gsap from "gsap"
import {ScrollTrigger} from "gsap/ScrollTrigger";
import {onMounted} from "vue";

gsap.registerPlugin(ScrollTrigger);

const scrollAnimation = () => {

  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: '.wrapper',
      start: 'center top',
      end: 'bottom end',
      markers: true,
      pin: true,
      pinSpacing: true
    }
  })

  tl.to('.animation-container', {
    scale: 0.6,
  })

  // tl.to('.animation-container', {
  //   x: 150,
  //   scale: 0.5,
  // })

  // tl.fromTo('.main-img .img1', {
  //   x: -600,
  //   y: -200,
  // }, {
  //   x: 0,
  //   y: 0,
  // })
  //
  // tl.fromTo('.main-img .img2', {
  //   x: -300,
  //   y: -700,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img3', {
  //   x: 700,
  //   y: -700,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img4', {
  //   x: 900,
  //   y: -700,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img5', {
  //   x: 500,
  //   y: 400,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img6', {
  //   x: 300,
  //   y: 400,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img7', {
  //   x: 200,
  //   y: 600,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.fromTo('.main-img .img8', {
  //   x: -500,
  //   y: 600,
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   x: 0,
  //   y: 0,
  //   scale: 1,
  //   opacity: 1
  // })
  //
  // tl.from('.main-img .img9', {
  //   x: -300,
  //   y: 600,
  //   scale: 2,
  //   opacity: 0
  // })
  //
  // tl.fromTo('.main-img', {
  //   scale: 2,
  //   opacity: 0
  // }, {
  //   scale: 1,
  //   opacity: 1,
  // })
  //
  // tl.fromTo('.img-uzb', {
  //   x: -2000,
  //   opacity: 0,
  // }, {
  //   x: 0,
  //   opacity: 1,
  // })
  //
  // tl.fromTo('.main-box', {
  //   x: 0,
  //   y: 0
  // }, {
  //   x: 300,
  //   scale: 0.6,
  // })

}

onMounted(() => {
  scrollAnimation();
})

</script>

<style scoped>

img {
  border-radius: 12px;
}

</style>
