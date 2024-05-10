<script>
import NavBar from '@/components/NavBar.vue'
import hotpotAnimation from '@/assets/Animated-Logo.mp4'
// core version + navigation, pagination modules:
// import Swiper from 'swiper'
// // import Swiper and modules styles
// import 'swiper/css'
// import 'swiper/css/navigation'
// import 'swiper/css/pagination'

export default {
  name: 'HouJia Hot Pot',
  components: {
    NavBar,
  },
  data () {
    return {
      hotpotAnimation
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
    // this.bannerSwiper()
  },

  beforeUnmount () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      const video = this.$refs.videoRef
      const viewportHeight = window.innerHeight
      const scrollY = window.scrollY
      if (scrollY <= viewportHeight) {
        video.play()
      } else {
        video.pause()
      }
    },
    // bannerSwiper () {
    //   new Swiper('.swiper', {
    //   // Optional parameters
    //     direction: 'vertical',
    //     loop: true,

    //     // If we need pagination
    //     pagination: {
    //       el: '.swiper-pagination'
    //     },

    //     // Navigation arrows
    //     navigation: {
    //       nextEl: '.swiper-button-next',
    //       prevEl: '.swiper-button-prev'
    //     },

    //     // And if we need scrollbar
    //     scrollbar: {
    //       el: '.swiper-scrollbar'
    //     }
    //   })
    // }

  }
}
</script>

<template>

    <body>
        <video ref="videoRef" autoplay muted loop>
            <source :src="hotpotAnimation" type="video/mp4">
        </video>
        <NavBar class="sticky top-0 z-30" />
        <div class="row banner-section">
            <div class="banner-all">
                <!-- Slider main container -->
                <!-- <Swiper class="swiper">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide">Slide 1</div>
                        <div class="swiper-slide">Slide 2</div>
                        <div class="swiper-slide">Slide 3</div>
                        ...
                    </div>
                    <div class="swiper-pagination"></div>

                    <div class="swiper-button-prev"></div>
                    <div class="swiper-button-next"></div>

                    <div class="swiper-scrollbar"></div>
                </Swiper> -->
            </div>
        </div>
    </body>
</template>
<style scoped>
.animation {
    width: 100;
    height: 500px;
}

.banner-section {
    background-color: cadetblue;
    height: 100vh;
    position: relative;
}

.banner-all {
    height: 600px;
    width: 60%;
    background-color: pink;
    position: absolute;
}

video {
    width: 100%;
    height: 100vh;
    object-fit: cover;
    object-position: 75%;
}
</style>