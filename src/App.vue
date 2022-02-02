<template>
  <div id="nav">
    <router-link :class="{ active: $route.name === 'Home' }" to="/"
      >Home</router-link
    >
    <router-link :class="{ active: $route.name === 'Cart' }" to="/Cart"
      >Cart</router-link
    >
  </div>
  <router-view />
</template>

<script>
export default {
  mounted() {
    this.$store.commit("updateCartFronStorage");
  },
};
</script>
<style lang="scss">
html,
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
body {
  background-color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: white;
  line-height: 30px;

  a {
    font-weight: bold;
    color: darkgray;
    text-decoration: none;
    margin: 0;
    font-size: 1.25rem;

    &.active {
      color: #2c3e50;
    }
  }
}
.text-color {
  text-align: center;
}
</style>
