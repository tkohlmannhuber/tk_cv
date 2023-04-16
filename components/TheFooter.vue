<template>
  <footer>
    <div class="bottom-bar">
      <ul>
        <li>Thomas Kohlmannhuber</li>
        <li>Lazarettgasse 41</li>
        <li>1090 Wien</li>
        <li><a href="tel:+4369917326885">+4369917326885</a></li>
        <li>
          <a href="mailto:thomas.kohlmannhuber@yahoo.de">
            thomas.kohlmannhuber@yahoo.de
          </a>
        </li>
      </ul>
      <div>
        <a href="https://nuxtjs.org"
          ><span>Made with</span><img src="~assets/images/nuxt.png" alt=""
        /></a>
        <a href="https://netlify.com"
          ><span>Hosted on</span><img src="~assets/images/netlify.png" alt=""
        /></a>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

.bottom-bar {
  padding: calc(var(--header-wrapper) / 2) var(--header-wrapper);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  gap: var(--gap);

  @include media('>=sm') {
    flex-direction: row;
    align-items: flex-end;
  }

  div {
    display: flex;
    gap: var(--gap);

    img {
      max-height: 1.2em;
    }

    a {
      display: flex;
      align-items: center;
      gap: calc(var(--gap) / 2);
    }
  }

  ul {
    display: flex;
    gap: var(--gap);
    flex-direction: column;

    @include media('>=lg') {
      flex-direction: row;
    }
  }
}
</style>
