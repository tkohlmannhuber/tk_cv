<template>
  <nav>
    <ul>
      <li>
        <a href="#">Whoami</a>
      </li>
      <li>
        <a href="#">Skills</a>
      </li>
      <li>
        <a href="#">Curriculum Vitea</a>
      </li>
      <li>
        <a href="#">Projects</a>
      </li>
      <li>
        <a href="#">Motivation</a>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
@import '~assets/scss/main';

ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: var(--gap);

  li {
    font-family: var(--headline-font);
    font-size: 2em;
    position: relative;

    &:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 3px;
    }

    &:nth-child(1):after {
      background: var(--color-primary);
    }
    &:nth-child(2):after {
      background: var(--color-secondary);
    }
    &:nth-child(3):after {
      background: var(--red);
    }
    &:nth-child(4):after {
      background: var(--yellow);
    }
    &:nth-child(5):after {
      background: var(--dark-green);
    }
  }
}
</style>
