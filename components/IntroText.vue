<template>
  <div>
    <h2 class="section-headline">Whoami<span class="lachs-text">!</span></h2>

    <article>
      <div class="intro-text-container">
        <p class="intro-text-main">
          Hi, my name is <span class="lachs-text">Thomas</span> Kohlmannhuber.
          I’m a frontend Developer based in Vienna. After working for 10 years
          as electrician in Upper Austria i decided to move to Vienna where i
          started learning Webdesign and Development at the SAE Vienna. After
          the first year of learning the basics of html, css and js i started my
          job as junior Developer at Floatwork.
        </p>
        <p class="intro-text">
          At Floatwork I’ve learned some more basics like working with git
          (making branches), using the terminal, making good coffee and how to
          work with Wordpress. After some smaller styling Tasks I’ve got my
          first own Project for Weinburgenland. While working on multiple
          different Wordpress projects i figured out that i want to work with
          newer technologies like Vue. I am pretty intrested in Web stuff, so
          i'm watching a lot of videos and reading Articles about Webdevelopment
          and Webdesign.
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
