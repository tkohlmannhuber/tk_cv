<template>
  <section>
    <div class="wrapper">
      <h2 class="section-headline">
        Back in the days<span class="lachs-text">!</span>
      </h2>
      <ul class="experience-list">
        <li
          v-for="year in experienceData"
          :key="year.year"
          class="experience-item"
        >
          <h3>
            <span>{{ year.year.start }}</span
            ><span>{{ year.year.end }}</span>
          </h3>
          <h4>{{ year.education }}</h4>
          <p v-if="year.task">{{ year.task }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      experienceData: [
        {
          year: {
            start: '1999',
            end: '2003',
          },
          education: 'Volkschule Kremsmünster',
        },
        {
          year: {
            start: '2003',
            end: '2007',
          },
          education: 'Hauptschule Kremsmünster',
        },
        {
          year: {
            start: '2007',
            end: '2008',
          },
          education: 'Handelsschule Kirchdorf',
        },
        {
          year: {
            start: '2008',
            end: '2019',
          },
          education: 'Greiner Bio One',
          task: 'Elektroanlagentechniker',
        },
        {
          year: {
            start: '2019',
            end: '2021',
          },
          education: 'SAE Wien',
          task: 'Webdesign & Webdevelopment',
        },
        {
          year: {
            start: '2020',
            end: '2021',
          },
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
    background: radial-gradient(
      circle,
      rgba(255, 255, 255, 0) 0%,
      rgba(0, 0, 0, 1) 60%,
      rgba(0, 0, 0, 1) 100%
    );
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
  background: rgba(0, 0, 0, 0.7);
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
    font-weight: var(--text-font-weight-medium);
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
