<template>
  <div class="card-grid-container">
    <div
      v-for="card in experienceCards"
      ref="card"
      :key="card.type"
      class="card"
      data-tilt
      data-tilt-scale="1.1"
    >
      <h3>{{ card.type }}</h3>
      <ul>
        <li v-for="item in card.items" :key="item.id">{{ item }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import VanillaTilt from 'vanilla-tilt'

export default {
  data() {
    return {
      experienceCards: [
        {
          type: 'Backend',
          items: ['php'],
        },
        {
          type: 'Frontend',
          items: ['css3', 'html 5', 'javascript'],
        },
        {
          type: 'CMS',
          items: ['Wordpress', 'sanity.io'],
        },
        {
          type: 'Frameworks',
          items: ['vue.js', 'nuxt.js', 'laravel', 'tailwind'],
        },
      ],
    }
  },

  mounted() {
    const element = this.$refs.card
    VanillaTilt.init(element, {
      gyroscope: true,
    })
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

.card-grid-container {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: calc(var(--gap) * 2);

  @include media('>=sm') {
    grid-template-columns: repeat(2, 1fr);
  }
  @include media('>=lg') {
    grid-template-columns: repeat(4, 1fr);
  }
}

.card {
  background: var(--card-bg);
  border-radius: var(--border-radius);
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: calc(var(--gap) * 2);
  position: relative;
  overflow: visible;
  transform-style: preserve-3d;
  transform: perspective(1000px);

  // &:hover {
  //   box-shadow: 0px 0px 48px -8px var(--color-secondary);
  // }

  &:before {
    content: '';
    position: absolute;
    width: 2.5em;
    height: 2.5em;
    border-radius: 100%;
    top: 0;
    transform: translateY(-50%) translateZ(50px);
  }

  &:first-child {
    h3:after {
      background: var(--color-primary);
    }

    &:before {
      border: 3px solid var(--yellow);
    }
  }
  &:nth-child(2) {
    h3:after {
      background: var(--color-secondary);
    }

    &:before {
      border: 3px solid var(--color-primary);
    }
  }
  &:nth-child(3) {
    h3:after {
      background: var(--yellow);
    }
    &:before {
      border: 3px solid var(--dark-green);
    }
  }
  &:last-child {
    h3:after {
      background: var(--dark-green);
    }

    &:before {
      border: 3px solid var(--color-secondary);
    }
  }

  ul li {
    text-align: center;
  }

  ul {
    transform: translateZ(50px);
  }
}

.card h3 {
  font-size: var(--card-headline-font-size);
  margin-bottom: var(--gap);
  position: relative;
  transform: translateZ(50px);

  &:after {
    content: '';
    position: absolute;
    width: 100%;
    height: 5px;
    bottom: 0;
    left: 0;
  }
}
</style>
