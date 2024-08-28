<script setup lang="ts">
import HeaderDesktopTop from "~/components/HeaderDesktopTop.vue";
import HeaderDesktopBottom from "~/components/HeaderDesktopBottom.vue";
</script>

<template>
<div class="header-desktop">
  <div class="container">
    <header-desktop-top />
    <img class="header-desktop__line" src="/svg/line.svg" alt="">
    <header-desktop-bottom />
  </div>
</div>
</template>

<style scoped lang="scss">
.header-desktop {
  &__line {
    width: 100%;
  }
}
</style>