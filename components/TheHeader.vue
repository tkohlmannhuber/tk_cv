<template>
  <header>
    <NuxtLink to="/">
      <Logo />
    </NuxtLink>

    <div
      class="burger-btn-container"
      :class="{ active: isActive }"
      @click="showMenu"
    >
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    }
  },
  methods: {
    showMenu() {
      this.$emit('showMenu')
      this.isActive = !this.isActive
    },
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

header {
  padding: var(--content-wrapper);
  display: flex;
  justify-content: space-between;
}

.burger-btn-container {
  width: 3.35em;
  height: 3.35em;
  border: 3px solid var(--color-secondary);
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-end;
  gap: 5px;
  padding: 0 8px 0 5px;
  z-index: 10000;

  .line {
    height: 3px;
    width: 100%;
    background: var(--white);
    border-radius: 10px;
    transition: 0.5s cubic-bezier(0.68, -0.6, 0.32, 1.6);
  }

  .line:first-child {
    width: 50%;
  }
  .line:last-child {
    width: 75%;
  }
}
.active .line:first-child {
  transform-origin: bottom;
  transform: rotatez(45deg) translate(-6px, 10px);
}

.active .line:nth-of-type(2) {
  transform-origin: top;
  transform: rotatez(-45deg);
}

.active .line:nth-of-type(3) {
  transform-origin: bottom;
  width: 55%;
  transform: translate(-2px, -4px) rotatez(45deg);
}
</style>
