<script setup lang="ts">
const catalogIsOpen = ref(false)
const openCatalog = () => {
  if (catalogIsOpen.value) {
    catalogIsOpen.value = false;
  } else {
    catalogIsOpen.value = true;
  }

}
</script>

<template>
<div class="header-desktop__bottom">
  <div @click="openCatalog" class="header-desktop__bottom-catalog">
    <span>Каталог</span>
    <div :class="{ active : catalogIsOpen }" class="header-desktop__bottom-catalog_burger">
      <span data-line="1"></span>
      <span data-line="2"></span>
      <span data-line="3"></span>
    </div>
  </div>
</div>
</template>

<style scoped lang="scss">
.header-desktop__bottom {
  &-catalog {
    font-weight: 400;
    font-size: 25px;
    line-height: 140%;
    color: #faf6f2;
    display: flex;
    align-items: center;
    cursor: pointer;
    gap: 8px;
    &_burger {
      & > span {
        background-color: #BB8C5F;
        width: 24px;
        height: 2px;
        transition: all .3s;
      }
      display: flex;
      flex-direction: column;
      gap: 4px;
      &.active {
        position: relative;
        span[data-line='1'] {
          transform: rotate(220deg);
          position: absolute;
        }
        span[data-line='2'] {
          display: none;
        }
        span[data-line='3'] {
          transform: rotate(310deg);
        }
      }
    }
  }
}
</style>