<!-- 菜单主体 -->
 <script setup lang="ts">
 import CategoryList from './CategoryList.vue'
 import DishList from './DishList.vue'
 </script>
 
 <template>
    <div class="menu">
        <CategoryList />
        <DishList />
    </div>
 </template>
 
 <style scoped>
    .menu {
        height: 70vh;
        width: 100vw;
        background-color: antiquewhite;
        display: flex;
        flex-direction: row;

    }
    .title {
        font-size: 50px;
        font-weight: bold;
    }
 
 </style>