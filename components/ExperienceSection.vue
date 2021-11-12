<template>
  <section id="skills" class="wrapper">
    <h2 class="section-headline">
      What I have learned<span class="lachs-text">!</span>
    </h2>
    <CardGrid />
  </section>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

.section-headline {
  margin-bottom: calc(var(--gap) * 2);

  @include media('>=md') {
    margin-bottom: calc(var(--gap) * 4);
  }
}
</style>
