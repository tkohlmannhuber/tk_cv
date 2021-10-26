<template>
  <section class="hero-section wrapper">
    <HeroHeadline />
    <HeroImage />
    <HeroIntro />
  </section>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

.hero-section {
  display: flex;
  flex-direction: column;
  gap: calc(var(--gap) * 2);

  @include media('>=md') {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    height: 100vh;
    place-items: center;
  }
}
</style>
