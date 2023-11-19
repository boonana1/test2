<template>
  <header>
    <h2>Игровые приставки</h2>
    <div class="buttons">
      <button class="search"><img :src="require(`@/assets/img/search.svg`)" alt=""></button>
      <button class="filter"><img :src="require(`@/assets/img/filter.svg`)" alt=""></button>
    </div>
  </header>
  <div class="categories">
    <button class="chips active">Все</button>
    <button class="chips ">Nintendo Switch</button>
    <button class="chips ">PS5</button>
    <button class="chips ">XBOX</button>
    <button class="chips ">Игры для приставок</button>
  </div>
  <ProductsList />
</template>

<script>
import ProductsList from './components/ProductsList.vue'

export default {
  name: 'App',
  components: {
    ProductsList
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  background: #f2f2f7;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-left: 16px;
  padding-right: 16px;
  max-width: 1240px;
  margin: 0 auto;
}

header {
  display: flex;
  padding-top: 8px;
  padding-bottom: 8px;
  justify-content: space-between;
}

header h2 {
  color: #000;
  font-size: 28px;
  font-style: normal;
  font-weight: 700;
  line-height: 34px;
  letter-spacing: -1px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

header .buttons {}

.buttons button {
  appearance: none;
  border: none;
  background: none;
}

.search,
.filter {
  width: 40px;
  height: 40px;
  padding: 8px;
}

.categories {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  justify-content: flex-start;
  gap: 8px;
  overflow-x: auto;
  margin-top: 8px;
  padding-bottom: 8px;
}

button.chips {
  display: flex;
  padding: 4px 12px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  appearance: none;
  border: none;
  border-radius: 100px;
  background: var(--backgrounds-primary, #FFF);
  box-shadow: 0px 6px 16px 0px rgba(120, 123, 156, 0.08);
  text-wrap: nowrap;
  text-align: center;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 22px;
  letter-spacing: -0.32px;
}

button.chips.active {
  border-radius: 100px;
  background: var(--accent-colors-indigo, #5856D6);
  color: #fff;
}
</style>
