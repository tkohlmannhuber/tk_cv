<template>
  <section id="cv">
    <div class="wrapper">
      <h2 class="section-headline" data-aos="fade">
        Back in the days<span class="lachs-text">!</span>
      </h2>
      <ul class="experience-list">
        <li
          v-for="year in experienceData"
          :key="year.job"
          class="experience-item"
        >
          <h3>
            <span>{{ year.year.start }}</span
            ><span>{{ year.year.end }}</span>
          </h3>
          <h4>{{ year.company }}</h4>
          <p v-if="year.job">{{ year.job }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  data() {
    return {
      experienceData: [
        {
          year: {
            start: '2008',
            end: '2019',
          },
          company: 'Greiner Bio One',
          job: 'Elektroanlagentechniker',
        },
        {
          year: {
            start: '2019',
            end: '2021',
          },
          company: 'SAE Wien',
          job: 'Webdesign & Webdevelopment Course',
        },
        {
          year: {
            start: '2020',
            end: '2025',
          },
          company: 'Floatwork',
          job: 'Fullstack Webdevelopment',
        },
      ],
    }
  },
  mounted() {
    AOS.init()
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

section {
  position: relative;
  margin-bottom: var(--section-spacing);

  &:after {
    content: '';
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background-image: url('~assets/images/bg-pattern.svg');
    background-size: 2000px;
    z-index: -1;
    opacity: 1;
  }
  &:before {
    content: '';
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background: radial-gradient(circle, hsla(0, 0%, 0%, 0), #000 60%, #000);
    opacity: 1;
  }

  & > div {
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 1000;
  }
}

.experience-list {
  display: grid;
  width: 100%;
  grid-template-columns: repeat(1, 1fr);
  gap: calc(var(--gap) * 4);
  border-radius: var(--border-radius);
  padding: 3em;

  @include media('>=sm') {
    grid-template-columns: repeat(2, 1fr);
    padding: 5em;
  }
  @include media('>=lg') {
    grid-template-columns: repeat(3, 1fr);
  }

  li {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    gap: calc(var(--gap) / 2);

    &:first-child {
      h3:after {
        background: var(--color-primary);
      }
    }
    &:nth-child(2) {
      h3:after {
        background: var(--color-secondary);
      }
    }
    &:nth-child(3) {
      h3:after {
        background: var(--yellow);
      }
    }
    &:nth-child(4) {
      h3:after {
        background: var(--yellow);
      }
    }
    &:nth-child(5) {
      h3:after {
        background: var(--color-secondary);
      }
    }
    &:last-child {
      h3:after {
        background: var(--dark-green);
      }
    }
  }

  h3 {
    font-size: 2.5em;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    line-height: 1;
    position: relative;
    margin-bottom: var(--gap);

    &:after {
      content: '';
      position: absolute;
      width: 100%;
      height: 5px;
      bottom: -20px;
      left: 0;
    }
  }

  h4 {
    font-family: var(--text-font);
    font-weight: var(--text-font-weight-bold);
    font-size: 1.5em;
    text-align: center;
    line-height: 1;
  }

  p {
    font-size: 1.2em;
    text-align: center;
  }
}
</style>
