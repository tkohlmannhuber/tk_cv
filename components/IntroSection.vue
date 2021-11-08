<template>
  <section class="wrapper">
    <IntroText />
    <MultipleCircle class="circle-bottom" />
  </section>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

section {
  display: flex;
  flex-direction: column;
  gap: var(--gap);

  .circle-top {
    @include media('>=md') {
      align-self: center;
    }
  }
  .circle-bottom {
    margin-top: var(--gap);
    align-self: center;
  }
}
</style>
