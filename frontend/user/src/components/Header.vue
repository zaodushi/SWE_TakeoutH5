<!-- 头部组件 -->
<script setup lang="ts">
interface StoreInfo {
  name: string
  rating: number
  deliveryTime: number
  deliveryFee: number
  minOrder: number
  distance: number
}

const storeInfo = {
  name: 'JB外卖 无良店家',
  rating: 4.7,
  deliveryTime: 30,
  deliveryFee: 5,
  minOrder: 20,
  distance: 1.5
}

const renderStars = (rating: number) => {
  return '★'.repeat(Math.floor(rating)) + '☆'.repeat(5 - Math.floor(rating))
}
</script>

<template>
  <div class="header">
    <div class="header__left">
      <div class="header__logo">
        <div class="logo-circle">JB</div>
      </div>
      <div class="header__info">
        <div class="header__title">{{ storeInfo.name }}</div>
        <div class="header__stats">
          <span class="rating">{{ renderStars(storeInfo.rating) }}</span>
          <span class="rating-number">{{ storeInfo.rating }}</span>
        </div>
        <div class="header__details">
          <span>{{ storeInfo.distance }}km</span>
          <span class="divider">|</span>
          <span>{{ storeInfo.deliveryTime }}分钟</span>
          <span class="divider">|</span>
          <span>配送费¥{{ storeInfo.deliveryFee }}</span>
        </div>
      </div>
    </div>
    <div class="header__right">
      <div class="notice">
        <span class="notice-tag">公告</span>
        <span>满{{ storeInfo.minOrder }}元起送</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  height: 10vh;
  width: 90vw;
  justify-content: space-between;
  align-items: center;
  background-color: bisque;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 0 15px;
}

.header__left {
  display: flex;
  align-items: center;
  gap: 15px;
}

.header__logo {
  display: flex;
  align-items: center;
}

.logo-circle {
  width: 50px;
  height: 50px;
  background-color: #ff6b6b;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: bold;
  font-size: 20px;
}

.header__info {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.header__title {
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

.header__stats {
  display: flex;
  align-items: center;
  gap: 8px;
}

.rating {
  color: #ffd700;
  letter-spacing: 2px;
}

.rating-number {
  color: #666;
  font-size: 14px;
}

.header__details {
  font-size: 12px;
  color: #666;
  display: flex;
  align-items: center;
  gap: 8px;
}

.divider {
  color: #ddd;
}

.header__right {
  display: flex;
  align-items: center;
}

.notice {
  background-color: #fff5f5;
  padding: 4px 8px;
  border-radius: 4px;
  font-size: 12px;
  color: #666;
}

.notice-tag {
  background-color: #ff6b6b;
  color: white;
  padding: 2px 4px;
  border-radius: 2px;
  margin-right: 4px;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .header {
    padding: 10px;
  }
  
  .header__title {
    font-size: 16px;
  }
  
  .logo-circle {
    width: 40px;
    height: 40px;
    font-size: 16px;
  }
  
  .header__details {
    font-size: 11px;
  }
  
  .notice {
    font-size: 11px;
  }
}

@media (max-width: 480px) {
  .header__right {
    display: none;
  }
}
</style>