<template>
  <div class="welcome-container">
    <!-- 歡迎標題 -->
    <h1 class="welcome-title">🛍️ 歡迎來到 Vue Shop Pro</h1>

    <!-- 介紹文字 -->
    <p class="welcome-description">
      你的現代化電商學習專案 ✨
      <br />
      我們將一起打造一個完整的購物網站！
    </p>

    <!-- 功能預告 -->
    <div class="features-preview">
      <div class="feature-item">🏪 商品展示</div>
      <div class="feature-item">🛒 購物車功能</div>
      <div class="feature-item">👤 會員系統</div>
      <div class="feature-item">📋 訂單管理</div>
    </div>

    <!-- 目前狀態 -->
    <div class="status-info">
      <p>
        📅 當前進度：<strong>{{ currentWeek }}</strong>
      </p>
      <p>
        🎯 本週目標：<strong>{{ weekGoal }}</strong>
      </p>
    </div>

    <!-- 動態計數器 -->
    <div class="counter-section">
      <p>
        你已經點擊了 <strong>{{ clickCount }}</strong> 次！
      </p>
      <button @click="increaseCount" class="click-button">
        🚀 點我試試 Vue 3 的響應式！
      </button>
    </div>
  </div>
</template>

<script setup>
// 📝 這是 Vue 3 的 Composition API 語法
import { ref } from 'vue'

const messyCode = {
  name: '測試',
  age: 25,
  hobbies: ['coding', 'reading', 'gaming']
}

const messyFunction = (param1, param2) => {
  return param1 + param2
}

// 定義響應式資料
const currentWeek = ref('第 1 週：專案初始化')
const weekGoal = ref('建立 Vue 3 開發環境')
const clickCount = ref(0)

// 定義方法
const increaseCount = () => {
  clickCount.value++
  console.log('🎉 按鈕被點擊了！目前次數：', clickCount.value)
}
</script>

<style scoped>
/* 🎨 組件專屬樣式 */
.welcome-container {
  max-width: 800px;
  margin: 2rem auto;
  padding: 2rem;
  text-align: center;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  color: white;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.welcome-title {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.welcome-description {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  line-height: 1.6;
}

.features-preview {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1rem;
  margin: 2rem 0;
}

.feature-item {
  background: rgba(255, 255, 255, 0.2);
  padding: 1rem;
  border-radius: 10px;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  transition: transform 0.3s ease;
}

.feature-item:hover {
  transform: translateY(-5px);
}

.status-info {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 1rem;
  margin: 2rem 0;
}

.counter-section {
  margin-top: 2rem;
}

.click-button {
  background: #ff6b6b;
  color: white;
  border: none;
  padding: 1rem 2rem;
  font-size: 1.1rem;
  border-radius: 50px;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
}

.click-button:hover {
  background: #ff5252;
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(255, 107, 107, 0.6);
}

.click-button:active {
  transform: translateY(0);
}

/* 🎯 響應式設計 */
@media (max-width: 768px) {
  .welcome-container {
    margin: 1rem;
    padding: 1rem;
  }

  .welcome-title {
    font-size: 2rem;
  }

  .features-preview {
    grid-template-columns: 1fr;
  }
}
</style>
