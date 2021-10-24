<template>
  <div>
    <transition name="nav">
      <OpenMenu v-if="showMenu" />
    </transition>
    <TheHeader @showMenu="showMenu = !showMenu" />
    <Nuxt />
    <TheFooter />
  </div>
</template>
<script>
export default {
  data() {
    return {
      showMenu: false,
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/main';

.nav-enter-active,
.nav-leave-active {
  transition: opacity 0.5s;
}
.nav-enter,
.nav-leave-active {
  opacity: 0;
}
</style>
