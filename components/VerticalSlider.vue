<template>
  <hooper
    class="slider-container"
    :vertical="true"
    :items-to-show="5"
    :center-mode="true"
  >
    <slide><h1>Greiner</h1></slide>
    <slide><h1>Greiner</h1></slide>
    <slide><h1>Greiner</h1></slide>
    <slide><h1>Greiner</h1></slide>
    <slide><h1>Greiner</h1></slide>
    <slide><h1>Greiner</h1></slide>

    <hooper-navigation slot="hooper-addons"></hooper-navigation>
    <hooper-pagination slot="hooper-addons"></hooper-pagination>
  </hooper>
</template>

<script>
import {
  Hooper,
  Slide,
  Pagination as HooperPagination,
  Navigation as HooperNavigation,
} from 'hooper'
import 'hooper/dist/hooper.css'
export default {
  components: {
    Hooper,
    Slide,
    HooperPagination,
    HooperNavigation,
  },
  data() {
    return {}
  },
}
</script>
<style lang="scss" scoped>
@import '~assets/scss/main';

.slider-container {
  height: 50vh;
  width: 30vw;
}
</style>
