<template>
  <!-- <button @click.prevent="slidePrev">prev</button>
  <button @click.prevent="slideNext">next</button> -->
  <hooper ref="carousel" :settings="hooperSettings">
    <slide class="single-slide">
      <img src="~/assets/images/project-slider/ipito-desk.png" alt="" />
    </slide>
    <slide class="single-slide">
      <img src="~/assets/images/project-slider/brew-desk.png" alt="" />
    </slide>
    <slide class="single-slide">
      <img src="~/assets/images/project-slider/wein-desk.png" alt="" />
    </slide>
  </hooper>
</template>

<script>
import { Hooper, Slide } from 'hooper'

export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      hooperSettings: {
        itemsToShow: 3,
        centerMode: true,
        wheelControl: false,
        infiniteScroll: true,
      },
    }
  },
}
</script>

<style lang="scss" scoped></style>
