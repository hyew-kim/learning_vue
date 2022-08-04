<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <nav class="menu">
    <a href="#">HOME</a><a href="#">PRODUCT</a><a href="#">ABOUT</a>
    <a href="#" v-for="e in menu" :key="e">{{ e }}</a>
    <a href="#" v-for="e in 3" :key="e">@</a>
  </nav>
  <div>
    <h4 :style="style">{{ products[0] }} room</h4>
    <p>{{ price1 }} won</p>
  </div>
  <div>
    <h4>{{ products[1] }} room</h4>
    <p>{{ price2 }} won</p>
  </div>
  <div>
    <h4>{{ products[2] }} room</h4>
    <p>{{ price2 }} won</p>
  </div>
  <div v-for="(product, i) in products" :key="i">
    <h4>{{ product }} 1 room</h4>
    <p>{{ price[i] }}</p>
  </div>
  <button>HALF</button>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      price1: 60,
      price2: 70,
      price: [60000, 50000, 30000],
      style: "color:blue",
      products: ["a", "b", "c"],
      menu: ["Home", "Products", "About"],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu {
  background: darkcyan;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
