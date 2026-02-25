<template>
  <div class="container">
    <header class="header">
      <HeaderNav />
    </header>
    <main class="main">
      <div class="left"></div>
      <div class="content"></div>
      <div class="right"></div>
    </main>
    <footer class="footer">
      <FooterIn />
    </footer>
  </div>
</template>
<script setup lang="ts">
import FooterIn from './components/footer-in.vue'
import HeaderNav from './components/header-nav.vue'
</script>
<style scoped lang="scss">
@use '@/styles/app.scss' as *;
</style>
