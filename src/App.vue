<template>
  <div class="container">
    <header class="header">
      <nav class="nav"></nav>
    </header>
    <main class="main">
      <div class="left"></div>
      <div class="content"></div>
      <div class="right"></div>
    </main>
    <footer class="footer"></footer>
  </div>
</template>
<script setup lang="ts"></script>
<style scoped lang="scss">
.container {
  .header {
    grid-area: header;
    background: palegoldenrod;
  }
  .footer {
    grid-area: footer;
    background: purple;
  }
  @include media(desktop) {
    .main {
      grid-area: main;
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      grid-template-areas: 'left content right';
      .left {
        grid-area: left;
      }
      .content {
        grid-area: content;
      }
      .right {
        grid-area: right;
      }
    }
  }
  @include media(tablet) {
    .main {
      grid-area: main;
      display: grid;
      grid-template-columns: 3fr 1fr;
      grid-template-areas: ' content right';
      .left {
        display: none;
      }
      .content {
        grid-area: content;
      }
      .right {
        grid-area: right;
      }
    }
  }

  @include media(mobile) {
    .main {
      grid-area: main;
      display: grid;
      grid-template-columns: 1fr;
      grid-template-areas: ' content';
      .left,
      .right {
        display: none;
      }
      .content {
        grid-area: content;
      }
    }
  }

  .main {
    .left {
      background: palegreen;
    }
    .content {
      background-color: palevioletred;
    }
    .right {
      background: peru;
    }
  }
}
</style>
