<template>
  <div id="app">
    <!-- 使用我們的自定義組件 -->
    <WelcomeShop />

    <!-- 原本的 Vue 標誌和連結可以保留或移除 -->
    <!-- <RouterView /> -->
  </div>
</template>

<script setup>
// 匯入我們建立的組件
import WelcomeShop from './components/WelcomeShop.vue'
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  min-height: 100vh;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
}

/* 移除預設邊距 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
