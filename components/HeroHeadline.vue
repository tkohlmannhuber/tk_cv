<template>
  <div class="headline-container">
    <h1>
      Hi, <span>I'm <span class="lachs-text">Thomas</span></span>
    </h1>
    <h2>Webdeveloper</h2>
    <a class="cta-link" href="mailto:thomas.kohlmannhuber@yahoo.de">
      Get in contact
      <span>
        <img src="~assets/images/icons/arrow-right.svg" alt="" />
      </span>
    </a>
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

.headline-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: calc(var(--gap) / 2);

  @include media('>=md') {
    grid-column: 1 / span 2;
  }

  h1 {
    display: flex;
    flex-direction: column;
    font-size: var(--hero-h1-font-size);
  }

  h2 {
    font-family: var(--text-font);
    font-weight: var(--text-font-weight-medium);
    font-size: 2.5em;
  }
}
</style>
