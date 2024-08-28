<script setup lang="ts">
import { ref } from 'vue';
import HeaderDesktop from "~/components/HeaderDesktop.vue";

let windowWidth = ref(0);

// Функция для обновления ширины экрана
const updateScreenWidth = () => {
  windowWidth.value = window.innerWidth
}

// Добавляем обработчики событий при монтировании компонента
onMounted(() => {
  window.addEventListener('DOMContentLoaded', updateScreenWidth);
  window.addEventListener('resize', updateScreenWidth);
})

// Удаляем обработчики событий при размонтировании компонента
onUnmounted(() => {
  window.removeEventListener('DOMContentLoaded', updateScreenWidth);
  window.removeEventListener('resize', updateScreenWidth);
})
</script>

<template>
  <header>
    <header-desktop />
  </header>
</template>

<style scoped lang="scss">
</style>