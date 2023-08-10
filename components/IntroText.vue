<template>
  <section class="intro-text-section">
    <h2 class="section-headline" data-aos="fade">
      About me<span class="lachs-text">!</span>
    </h2>

    <article>
      <div class="intro-text-container">
        <p class="intro-text-main" data-aos="fade-up">
          Hi, I'm <span class="lachs-text">Thomas Kohlmannhuber</span>, a
          frontend developer based in Vienna, specializing in building websites
          with WordPress and Vue.js. With a passion for coding and a keen eye
          for design, I strive to deliver unique and dynamic web experiences
          that meet the specific needs of my clients. Whether you are a small
          business owner, a startup, or a large corporation, I have the
          expertise and skill set to create a website that not only looks great
          but also functions flawlessly.
        </p>
        <p class="intro-text" data-aos="fade-up" data-aos-delay="100">
          My approach to web development is rooted in collaboration,
          communication, and attention to detail. I take the time to listen to
          my clients and understand their goals and objectives before beginning
          any project. From there, I work closely with them to develop a
          customized solution that meets their specific needs. With a focus on
          user experience and accessibility, I ensure that every website I build
          is not only visually stunning but also easy to navigate and use.
          Whether you need a simple brochure site or a complex e-commerce
          platform, I am committed to delivering a website that exceeds your
          expectations.
        </p>
      </div>
    </article>
  </section>
</template>
<script>
import AOS from 'aos'
import 'aos/dist/aos.css'
export default {
  mounted() {
    AOS.init()
  },
}
</script>

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
