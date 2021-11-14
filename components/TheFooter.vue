<template>
  <footer>
    <div class="bottom-bar">
      <ul>
        <li>Thomas Kohlmannhuber</li>
        <li>Flachgasse 49</li>
        <li>1150 Wien</li>
        <li><a href="tel:+4369917326885">+4369917326885</a></li>
        <li>
          <a href="mailto:thomas.kohlmannhuber@yahoo.de">
            thomas.kohlmannhuber@yahoo.de
          </a>
        </li>
      </ul>
      <div>
        <a href="https://nuxtjs.org">Made with <img src="" alt="" /></a>
        <a href="https://netlify.com">Hosted on <img src="" alt="" /></a>
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
  }

  ul {
    display: flex;
    gap: var(--gap);
    flex-direction: column;

    @include media('>=md') {
      flex-direction: row;
    }
  }
}
</style>
