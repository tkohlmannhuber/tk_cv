<template>
  <NavList />
</template>

<style lang="scss" scoped>
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
