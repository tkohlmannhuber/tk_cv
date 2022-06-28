<template>
  <div class="hero-intro-text">
    <Circles />
    <h3 class="lachs-text">Whoami</h3>
    <p>
      Living in Vienna, working as a Web developer and looking for a new job!
    </p>
    <p>
      Hey, I'm looking for a new challenge to build cool stuff with modern web
      technologies and techniques!
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

.hero-intro-text {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
  position: relative;
  max-width: 30ch;

  h3 {
    font-family: var(--text-font);
    font-weight: var(--text-font-weight-bold);
    font-size: 1.5em;
  }

  p {
    font-size: 1.375em;
    &:last-child {
      color: var(--white-light);
    }
  }

  svg {
    position: absolute;
    right: 0;
    top: -50%;
    transform: translateY(50%);
  }
}
</style>
