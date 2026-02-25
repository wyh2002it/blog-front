<template>
  <div class="index-card">
    <div class="card">
      <div class="tools">
        <div class="circle">
          <span class="red box"></span>
        </div>
        <div class="circle">
          <span class="yellow box"></span>
        </div>
        <div class="circle">
          <span class="green box"></span>
        </div>
      </div>
      <div class="card-content">
        <div class="user-image">
          <img src="../assets/image/头像.jpg" alt="用户头像" />
        </div>
        <div class="user-name">恋旧</div>
        <div class="user-description">这是我的个人博客</div>
        <div class="user-link"></div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.index-card {
  .card {
    width: 280px;
    height: 340px;
    background-color: #f8fbfe;
    border-radius: 8px;
    z-index: 1;
    .tools {
      display: flex;
      align-items: center;
      padding: 9px;
      .circle {
        padding: 0 4px;
        .box {
          display: inline-block;
          align-items: center;
          width: 10px;
          height: 10px;
          padding: 1px;
          border-radius: 50%;
        }
        .red {
          background-color: #ff605c;
        }

        .yellow {
          background-color: #ffbd44;
        }

        .green {
          background-color: #00ca4e;
        }
      }
    }
    .card-content {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 20px;
      gap: 20px;
      height: 100%;
      .user-image {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        overflow: hidden;
        img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }
      .user-description {
        color: #666;
        font-size: 14px;
      }
    }
  }
}
</style>
