<template>
  <section class="wrapper">
    <Circles class="circle-top" />
    <IntroText />
    <SingleCircle class="circle-bottom" />
  </section>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

section {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
  margin-bottom: var(--section-spacing);

  .circle-top {
    @include media('>=md') {
      align-self: center;
    }
  }
  .circle-bottom {
    align-self: center;
  }
}
</style>
