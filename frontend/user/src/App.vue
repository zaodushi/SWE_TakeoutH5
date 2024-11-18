<script setup>
import Header from './components/Header.vue'
import Menu from './components/Menu.vue'
import Cart from './components/Cart.vue'
</script>

<template>
  <div class="app">
    <Header />
    <Menu />
    <Cart />
  </div>
</template>

<style scoped>
.app{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 0;

}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
