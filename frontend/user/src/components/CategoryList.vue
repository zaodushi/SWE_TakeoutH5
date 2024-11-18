<!-- 左侧分类列表 -->
<script setup lang="ts">
import { ref } from 'vue';

const categories = ref([
    { id: 1, name: '寿司' },
    { id: 2, name: '拉面' },
    { id: 3, name: '小吃' },
    { id: 4, name: '甜点' },
    { id: 5, name: '饮料' }
]);

const selectedCategory = ref(null);

const selectCategory = (category) => {
    selectedCategory.value = category;
};
</script>

<template>
    <div class="category-list">
        <ul>
            <li v-for="category in categories" :key="category.id" @click="selectCategory(category)">
                {{ category.name }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.category-list {
    background-color: black;
    height: 70vh;
    width: 15vw;
    color: white;
    overflow-y: auto;
}

.category-list ul {
    list-style-type: none;
    padding: 0;
}

.category-list li {
    padding: 10px;
    cursor: pointer;
}

.category-list li:hover {
    background-color: #333;
}
</style>
