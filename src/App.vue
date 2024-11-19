<template>
  <div id="app">
    <Navbar />
    <ProductPage />
  </div>
</template>

<script>
import ProductPage from './components/ProductPage.vue';
import Navbar from './components/Navbar.vue';

export default {
  components: {
    ProductPage,
    Navbar,
  },
};
</script>

<style>
#app {
  font-family: Montserrat;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50;
  margin-top: 60px; */
}
</style>