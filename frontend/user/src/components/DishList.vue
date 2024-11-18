<script setup lang="ts">
import { ref } from 'vue';

interface Dish {
    id: number;
    name: string;
    category: string;
    price: number;
    quantity: number;
}

const dishes = ref<Dish[]>([
    { id: 1, name: '三文鱼寿司', category: '寿司', price: 10, quantity: 0 },
    { id: 2, name: '鳗鱼寿司', category: '寿司', price: 12, quantity: 0 },
    { id: 3, name: '地狱拉面', category: '拉面', price: 15, quantity: 0 },
    { id: 4, name: '番茄拉面', category: '拉面', price: 13, quantity: 0 },
    { id: 5, name: '章鱼小丸子', category: '小吃', price: 8, quantity: 0 },
    { id: 6, name: '大阪烧', category: '小吃', price: 10, quantity: 0 },
]);
console.log(dishes);

const increment = (dish: Dish) => {
    dish.quantity++;
};

const decrement = (dish: Dish) => {
    if (dish.quantity > 0) {
        dish.quantity--;
    }
};
</script>

<template>
    <div class="dish-list">
        <div v-for="dish in dishes" :key="dish.id" class="dish-item">
            <div class="dish-info">
                <h3>{{ dish.name }}</h3>
                <p>{{ dish.category }}</p>
                <p>${{ dish.price }}</p>
            </div>
            <div class="quantity-controls">
                <button @click="decrement(dish)">-</button>
                <span>{{ dish.quantity }}</span>
                <button @click="increment(dish)">+</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.dish-list {
    width: 85vw;
    height: 70vh;
    overflow-y: auto;
}

.dish-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 1px solid #ccc;
    padding: 10px;
    margin: 10px 0;
    height: 15vh;
}

.dish-info {
    flex: 1;
}

.quantity-controls {
    display: flex;
    align-items: center;
}

.quantity-controls button {
    margin: 0 5px;
}
</style>