<template>
  <figure>
    <img src="~assets/images/hero-img.png" alt="" />
  </figure>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

figure {
  align-self: center;
  position: relative;

  @include media('>=md') {
    position: absolute;
    left: 0;
    transform: translate(-50%, 3em);
  }

  // &:after {
  //   content: '';
  //   width: 100%;
  //   height: 100%;
  //   position: absolute;
  //   left: 0;
  //   top: 0;
  //   background: linear-gradient(
  //     90deg,
  //     rgba(255, 255, 255, 0) 50%,
  //     rgba(0, 0, 0, 1) 100%
  //   );
  // }
  // &:before {
  //   content: '';
  //   width: 100%;
  //   height: 100%;
  //   position: absolute;
  //   left: 0;
  //   top: 0;
  //   background: var(--black-overlay);
  // }
}
</style>
