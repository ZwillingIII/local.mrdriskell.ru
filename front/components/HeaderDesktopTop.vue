<script setup lang="ts">
const phone = ref('+7 952 552-52-52');
const email = ref('Mr.Driskell@mail.ru');
const cartPrice = ref('38 000')
</script>

<template>
<div class="header-desktop__top">
  <div class="header-desktop__top-contacts">
    <a class="header-desktop__top-item">
      <img src="/svg/phone.svg" alt="">
      <span>{{ phone }}</span>
    </a>
    <a class="header-desktop__top-item">
      <img src="/svg/mail.svg" alt="">
      <span>{{ email }}</span>
    </a>
  </div>
  <div class="header-desktop__top-logo">
    <img src="/svg/logo.svg" alt="">
  </div>
  <div class="header-desktop__top-navs">
    <a class="header-desktop__top-navs_item">
      <div class="header-desktop__top-navs_price">{{ cartPrice }} ₽</div>
      <img src="/svg/cart.svg" alt="">
    </a>
    <a class="header-desktop__top-navs_item">
      <img src="/svg/favorite.svg" alt="">
    </a>
    <a class="header-desktop__top-navs_item">
      <img src="/svg/personal.svg" alt="">
    </a>
  </div>
</div>
</template>

<style scoped lang="scss">
.header-desktop__top {
  padding: 34px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  img {
    width: 28px;
    height: 28px;
  }
  &-contacts {
    display: flex;
    flex-direction: row;
    gap: 50px;
  }
  &-item {
    display: flex;
    flex-direction: row;
    align-content: center;
    gap: 10px;
    span {
      font-weight: 400;
      font-size: 15px;
      line-height: 150%;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
  }
}
</style>