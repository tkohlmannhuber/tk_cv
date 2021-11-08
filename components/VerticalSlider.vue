<template>
  <hooper
    class="slider-container"
    :vertical="true"
    :items-to-show="1"
    :center-mode="true"
  >
    <slide v-for="year in experienceData" :key="year.year" class="single-slide">
      <h3>{{ year.year }}</h3>
      <h4>{{ year.education }}</h4>
      <p v-if="year.task">{{ year.task }}</p>
    </slide>

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
    return {
      experienceData: [
        {
          year: '1999 - 2003',
          education: 'Volkschule Kremsmünster',
        },
        {
          year: '2004 - 2008',
          education: 'Hauptschule Kremsmünster',
        },
        {
          year: '2008 - 2019',
          education: 'Greiner Bio One',
          task: 'Elektroanlagentechniker',
        },
        {
          year: '2019 - 2021',
          education: 'SAE Wien',
          task: 'Webdesign & Webdevelopment',
        },
        {
          year: '2020 - 2021',
          education: 'Floatwork',
          task: 'Wordpress Webdevelopment',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
@import '~assets/scss/main';

.slider-container {
  width: 70vw;
  margin-left: auto;
  margin-bottom: var(--section-spacing);
}

.hooper-prev {
  background: red;
}

.single-slide {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: calc(var(--gap) / 2);
  padding: var(--gap);

  h3 {
    font-size: 2em;
  }
  h4 {
    font-size: 1.8em;
  }
}
</style>
