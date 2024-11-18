<!-- 头部组件 -->
 <script setup lang="ts">
 
 </script>
 
 <template>
    <div class="header">
        <div class="header__left">
            <div class="header__title">JB外卖 无良店家</div>
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
 }
 .header__left {
     display: flex;
     align-items: center;
 }
 .header__title {
     font-size: 50px;
     font-weight: bold;
 }
 
 </style>