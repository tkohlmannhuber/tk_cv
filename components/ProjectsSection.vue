<template>
  <section id="projects" class="prjects-section wrapper">
    <h2 class="section-headline wrapper">
      Projects<span class="lachs-text">!</span>
    </h2>
    <div class="projects-grid">
      <a href="https://ipito.surf">
        <img
          src="~/assets/images/project-slider/ipito-desk.png"
          alt="Ipito Website image"
        />
        <div>
          <h3>IPITO</h3>
          <ul>
            <li>Final Project SAE</li>
            <li>Vue.js & Laravel</li>
          </ul>
        </div>
      </a>
      <!-- <a href="https://brewage.711.at" class="single-slide">
        <img src="~/assets/images/project-slider/brew-desk.png" alt="" />
        <div>
          <h3>Brewage</h3>
        </div>
      </a>
      <a href="https://weinburgenland.711.at" class="single-slide">
        <img src="~/assets/images/project-slider/wein-desk.png" alt="" />
        <div>
          <h3>Weinburgenland</h3>
        </div>
      </a> -->
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showOverlay: false,
    }
  },

  methods: {
    overlayActive() {
      this.showOverlay = !this.showOverlay
    },
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

h2 {
  margin-bottom: calc(var(--gap) * 4);
}

.projects-grid {
  display: grid;
  gap: var(--gap);
  grid-template-columns: 80vw;
  @include media('>=sm') {
    grid-template-columns: 80vw;
  }
  @include media('>=md') {
    grid-template-columns: 60vw;
  }

  @include media('>=xxl') {
    grid-template-columns: 50vw;
  }

  a {
    position: relative;
    &:hover {
      div {
        opacity: 1;
      }
    }
  }

  a > div {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background: var(--black-overlay);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: var(--gap);
    border-radius: var(--border-radius);
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
  }

  h3 {
    font-size: 3em;
    position: relative;

    &:after {
      content: '';
      position: absolute;
      width: 100%;
      bottom: -5px;
      left: 0;
      height: 5px;
      background: var(--yellow);
    }
  }

  img {
    border-radius: var(--border-radius);
  }
}
</style>
