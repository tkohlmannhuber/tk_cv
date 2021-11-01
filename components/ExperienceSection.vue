<template>
  <section class="wrapper">
    <h2 class="section-headline">
      What i have learned<span class="lachs-text">!</span>
    </h2>
    <CardGrid />
  </section>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

section {
  margin-bottom: var(--section-spacing);
}
.section-headline {
  text-align: center;
  margin-bottom: calc(var(--gap) * 2);
}
</style>
