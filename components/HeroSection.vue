<template>
  <section class="hero-section wrapper">
    <HeroHeadline class="hero-headline" />
    <HeroIntro class="hero-intro-text" />
    <HeroImage class="hero-image" />
  </section>
</template>
<script>
import { gsap } from 'gsap'
export default {
  mounted() {
    // Create a GSAP timeline
    const timeline = gsap.timeline()

    timeline
      .from('.hero-image', { duration: 1, opacity: 0 })
      .from('.hero-headline', { duration: 0.5, opacity: 0 })
      .from('.hero-intro-text', { duration: 0.5, opacity: 0 })
    timeline.play()
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

.hero-section {
  display: flex;
  flex-direction: column;
  gap: calc(var(--gap) * 2);
  padding-top: 7em;

  @include media('>=md') {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    height: 100vh;
    place-items: center;
  }
}
</style>
