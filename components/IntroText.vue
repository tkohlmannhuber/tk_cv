<template>
  <div>
    <h2 class="section-headline">Whoami<span class="lachs-text">!</span></h2>

    <article>
      <div class="intro-text-container">
        <p class="intro-text-main">
          Hi, my name is <span class="lachs-text">Thomas</span> Kohlmannhuber.
          I’m a frontend developer based in Vienna. After working for 10 years
          as an electrician in Upper Austria, I decided to move to Vienna where
          I started learning Web design and development at the SAE Vienna. After
          the first year of learning the basics of HTML, CSS and JS, I started
          my job as a junior developer at Floatwork.
        </p>
        <p class="intro-text">
          At Floatwork, I’ve learned some more basics like working with git
          (making branches), using the terminal, making good coffee and how to
          work with Wordpress. After some smaller styling tasks, I’ve got my
          first own project for Weinburgenland. While working on multiple
          different Wordpress projects I figured out that I want to work with
          newer technologies like Vue. I am pretty interested in Web stuff, so
          I’m watching a lot of videos and reading articles about Web
          development and Web design.
        </p>
      </div>
    </article>
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

article {
  display: grid;
  gap: var(--gap);
}

.intro-text-container {
  display: grid;
  gap: var(--gap);

  @include media('>=md') {
    grid-template-columns: repeat(2, 1fr);
    gap: 15%;
  }
}

.intro-text-main {
  font-size: 1.14em;
}
.intro-text {
  color: var(--white-light);
  margin-bottom: var(--gap);
}
</style>
