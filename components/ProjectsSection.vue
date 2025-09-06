<template>
  <section id="projects" class="prjects-section wrapper">
    <h2 class="section-headline wrapper">
      Projects<span class="lachs-text">!</span>
    </h2>
    <div class="projects-grid">
      <a href="https://mcs.at" class="single-slide">
        <img src="~/assets/images/project-slider/mcs-desk.png" alt="" />
        <div>
          <h3>MCS</h3>
        </div>
      </a>
      <a href="https://wasserspass.net" class="single-slide">
        <img src="~/assets/images/project-slider/wasserspass-desk.png" alt="" />
        <div>
          <h3>Wasserspass</h3>
        </div>
      </a>
      <a href="https://forumverfassung.at" class="single-slide">
        <img src="~/assets/images/project-slider/sfv.png" alt="" />
        <div>
          <h3>Forumverfassung</h3>
        </div>
      </a>
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
  gap: calc(var(--gap) * 2);
  grid-template-columns: 80vw;
  @include media('>=sm') {
    grid-template-columns: 1fr;
  }
  @include media('>=md') {
    grid-template-columns: repeat(2, 1fr);
  }

  @include media('>=xxl') {
    grid-template-columns: repeat(3, 1fr);
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
    font-size: 2em;
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
