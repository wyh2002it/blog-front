<template>
  <div class="header-nav">
    <div class="nav-container">
      <!-- Logo区域 -->
      <div class="logo-section">
        <div class="logo">
          <span class="logo-icon">LOGO</span>
        </div>
      </div>

      <!-- 搜索栏 -->
      <div class="search-section">
        <div class="search-box">
          <input type="text" placeholder="搜索..." class="search-input" />
          <button class="search-btn">
            <span class="search-icon icon-placeholder">🔍</span>
          </button>
        </div>
      </div>

      <!-- 导航菜单 -->
      <div class="nav-section">
        <nav class="navigation">
          <ul class="nav-list">
            <li class="nav-item">
              <a href="#" class="nav-link">
                <span class="nav-icon icon-placeholder">🏠</span>
                <span class="nav-text">首页</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">
                <span class="nav-icon icon-placeholder">📚</span>
                <span class="nav-text">文章</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">
                <span class="nav-icon icon-placeholder">🏷️</span>
                <span class="nav-text">标签</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">
                <span class="nav-icon icon-placeholder">👤</span>
                <span class="nav-text">关于</span>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
// 组件逻辑可以在这里添加
</script>

<style scoped lang="scss">
@use '@/styles/app.scss' as *;

.header-nav {
  background-color: #ffffff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 0 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 60px;

  @media (max-width: 840px) {
    flex-direction: column;
    height: auto;
    padding: 10px 0;
  }
}

.logo-section {
  display: flex;
  align-items: center;

  .logo {
    display: flex;
    align-items: center;

    .logo-icon {
      font-size: 24px;
      font-weight: bold;
      color: #333;
    }
  }
}

.search-section {
  flex: 1;
  max-width: 400px;
  margin: 0 20px;

  .search-box {
    display: flex;
    border: 1px solid #ddd;
    border-radius: 24px;
    overflow: hidden;

    .search-input {
      flex: 1;
      padding: 8px 16px;
      border: none;
      outline: none;
      font-size: 14px;
    }

    .search-btn {
      background: #f5f5f5;
      border: none;
      padding: 8px 16px;
      cursor: pointer;
      display: flex;
      align-items: center;

      .search-icon {
        font-size: 16px;
      }
    }
  }

  @media (max-width: 840px) {
    order: 3;
    max-width: 100%;
    margin: 10px 0 0;
  }
}

.nav-section {
  .navigation {
    .nav-list {
      display: flex;
      list-style: none;
      margin: 0;
      padding: 0;

      .nav-item {
        margin-left: 20px;

        &:first-child {
          margin-left: 0;
        }

        .nav-link {
          display: flex;
          align-items: center;
          text-decoration: none;
          color: #333;
          padding: 8px 12px;
          border-radius: 4px;
          transition: background-color 0.3s;

          &:hover {
            background-color: #f5f5f5;
          }

          .nav-icon {
            margin-right: 6px;
            font-size: 16px;

            /* 为实际图标预留的类名 */
            &.icon-placeholder {
              display: inline-flex;
              align-items: center;
              justify-content: center;
              width: 20px;
              height: 20px;
            }
          }

          .nav-text {
            font-size: 14px;
          }
        }
      }
    }
  }

  @media (max-width: 840px) {
    order: 2;
    width: 100%;
    margin-top: 10px;

    .navigation {
      .nav-list {
        justify-content: center;

        .nav-item {
          margin: 0 10px;
        }
      }
    }
  }
}

// 在小屏幕上的响应式调整
@media (max-width: 840px) {
  .nav-container {
    width: 100%;
    flex-wrap: wrap;
  }

  .logo-section {
    order: 1;
  }
}
</style>
