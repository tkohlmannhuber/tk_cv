<template>
  <div>
    <!-- <div ref="cursor_outer" class="cursor_outer"></div>
    <div ref="cursor_inner" class="cursor_inner"></div> -->
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
  // mounted() {
  //   this.setCursorOuter()
  //   this.setCursorInner()
  // },

  // methods: {
  //   setCursorOuter() {
  //     const cursor = this.$refs.cursor_outer
  //     document.addEventListener('mousemove', (e) => {
  //       cursor.style.top = e.pageY + 'px'
  //       cursor.style.left = e.pageX + 'px'
  //     })
  //   },
  //   setCursorInner() {
  //     const cursor = this.$refs.cursor_inner
  //     document.addEventListener('mousemove', (e) => {
  //       cursor.style.top = e.pageY + 'px'
  //       cursor.style.left = e.pageX + 'px'
  //     })
  //   },
  // },
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
