<script setup lang="ts">
import HeaderComponent from "~/components/HeaderComponent.vue";
</script>

<template>
  <div>
    <header-component />
    <main>
      <NuxtPage />
    </main>
  </div>
</template>

<style lang="scss">
@font-face {
  font-family: 'Jost';
  src: url("/fonts/jost/static/Jost-Light.ttf");
}

.container {
  max-width: 1390px;
  padding: 0 30px;
  margin: 0 auto;
  position: relative;
}

body {
  background: #050402;
  font-family: 'Jost', sans-serif;
  color: #faf6f2;
}
</style>