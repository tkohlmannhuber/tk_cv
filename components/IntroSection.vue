<template>
  <section class="wrapper">
    <Circles />
    <IntroText />
    <SingleCircle class="circle" />
  </section>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  gap: var(--gap);

  .circle {
    align-self: center;
  }
}
</style>
