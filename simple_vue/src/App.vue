<template>
  <img alt="Vue logo" src="./assets/logo.png" />
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
      style: "color:blue",
      products: ["a", "b", "c"],
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
  margin-top: 60px;
}
</style>
