<template>
  <footer class="footer-in">
    <!-- 版权信息区域 -->
    <div class="footer-bottom">
      <div class="footer-copyright">
        <p>&copy; {{ currentYear }} 我的博客. 保留所有权利.</p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>

<style scoped lang="scss">
.footer-in {
  background-color: #2c3e50;
  color: #ecf0f1;
  margin-top: auto;
}

.footer-bottom {
  border-top: 1px solid #34495e;

  .footer-copyright {
    display: flex;
    flex-direction: column;
    align-items: center;

    p {
      color: #bdc3c7;
      font-size: 14px;
    }

    @media (max-width: 768px) {
      flex-direction: column;
      text-align: center;
    }
  }
}
</style>
