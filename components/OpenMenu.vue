<template>
  <nav>
    <ul>
      <li>
        <a href="#whoami" @click="closeNav">Whoami</a>
      </li>
      <li>
        <a href="#skills" @click="closeNav">Skills</a>
      </li>
      <li>
        <a href="#cv" @click="closeNav">Curriculum Vitea</a>
      </li>
      <li>
        <a href="#projects" @click="closeNav">Projects</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {}
  },

  methods: {
    closeNav() {
      this.$emit('closeNav')
    },
  },
}
</script>

<style lang="scss" scoped>
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

nav {
  position: fixed;
  height: 100vh;
  width: 100%;
  background: var(--nav-overlay);
  display: grid;
  place-items: center;
  left: 0;
  top: 0;
  z-index: 10000;
}
</style>
