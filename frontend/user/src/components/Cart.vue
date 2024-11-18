<!-- 购物车组件 -->
<script setup lang="ts">

</script>

<template>
    <div class="cart">
        <div class="cart-header">
            <span>购物车</span>
            <span>清空</span>
        </div>  
    </div>
</template>

<style scoped>
.cart {
    position: fixed;
    right: 15vw;
    bottom: 5vw;
    width: 80vw;
    height: 8vh;
    background-color: #000000;
    box-shadow: -2px 0 2px rgba(0, 0, 0, 0.1);
    z-index: 100;
    padding: 20px;
    box-sizing: border-box;
    overflow-y: auto;
}
.cart-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 20px;
}
.cart-header span {
    color: azure;
    cursor: pointer;
}
</style>