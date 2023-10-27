<template>
  <div class="min-h-screen">
    <div class="wrapper min-h-screen">
      <div class="min-h-screen relative">
        <div class="container-animation min-h-screen w-full h-full absolute inset-0">
          <div class="relative w-full">
            <div class="absolute w-full h-full top-[0] right-[0]">
              <div class="container h-full">
                <img src="../assets/5.png" alt=""
                     class="absolute img cursor-pointer scale-[1.7] top-[104px] left-[-50px] z-[999]" id="image-1"/>
                <img src="../assets/2.png" alt=""
                     class="absolute img cursor-pointer scale-[1.7] top-[-90px] left-[120px] z-[999]" id="image-2"/>
                <img src="../assets/3.png" alt=""
                     class="absolute img cursor-pointer scale-[2.7] top-[-110px] right-[160px] z-[999]" id="image-3"/>
                <img src="../assets/4.png" alt=""
                     class="absolute img cursor-pointer scale-[2.7] top-[190px] right-[-160px] z-[999]" id="image-4"/>
                <img src="../assets/1.png" alt=""
                     class="absolute img cursor-pointer scale-[2.7] bottom-[160px] right-[-140px] z-[999]"
                     id="image-5"/>
                <img src="../assets/6.png" alt=""
                     class="absolute img cursor-pointer scale-[2.7] bottom-[50px] right-[180px] z-[999]" id="image-6"/>
                <img src="../assets/7.png" alt=""
                     class="absolute img cursor-pointer scale-[3] bottom-[-180px] right-[40%] z-[999]" id="image-7"/>
                <img src="../assets/8.png" alt=""
                     class="absolute img cursor-pointer scale-[2.8] bottom-[-40px] left-[190px] z-[999]" id="image-8"/>
                <img src="../assets/9.png" alt=""
                     class="absolute img cursor-pointer scale-[3] top-[50%] left-[-180px] z-[999]" id="image-9"/>
              </div>
            </div>
            <div class="relative overflow-hidden">
              <div
                  class="overlay absolute z-[999] top-0 right-0 w-full h-full flex-col flex items-center justify-center"
                  id="image-uzb"
              >
                <img src="../assets/uzbekistans.png" alt="">
              </div>
              <video src="../assets/uzbekistans.mp4" class="w-full min-h-screen object-cover" autoplay playsinline muted
                     loop/>
              <div class="absolute top-0 right-0 w-full h-full bg-[#00000040] flex items-end justify-center">
                <a href="https://uzbekistans.club/projects/ozbekistonlik" class="player mb-[260px]">
                  <PlayButton/>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import {gsap} from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger"
import {onMounted} from "vue";
import PlayButton from "../UIComponent/PlayButton.vue"


gsap.registerPlugin(ScrollTrigger)

function animatePage() {
  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: '.wrapper',
      start: 'top',
      end: 'bottom -300px',
      markers: false,
      scrub: 5,
      pin: true,
      pinSpacing: true,
      toggleActions: 'play none none reverse'
    }
  })

  tl.to('.container-animation', {
    scale: 0.4,
    x: '5%'
  })

  tl.from('#image-1', {
    x: -600,
    y: -200,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-2', {
    x: -300,
    y: -700,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-3', {
    x: 700,
    y: -700,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-4', {
    x: 900,
    y: -700,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-5', {
    x: 500,
    y: 400,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-6', {
    x: 300,
    y: 600,
    // scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-7', {
    x: 200,
    y: 600,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-8', {
    x: -500,
    y: 700,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-9', {
    x: -400,
    y: 600,
    scale: 3,
    opacity: 0
  }, "-=0.5")

  tl.from('#image-uzb', {
    x: -2000,
    opacity: 0,
  }, "-=0.5")

  tl.to('.container-animation', {
    scale: 0.3,
    x: '20%'
  })

  tl.to('#image-uzb', {
    x: 0,
    opacity: 1
  })


}


onMounted(() => {
  animatePage()
})

</script>

<style scoped>

.img {
  border-radius: 12px;
}

</style>