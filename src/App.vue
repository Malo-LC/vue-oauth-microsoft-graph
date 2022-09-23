<template>
  <div>
    <base-header />
    <home-page />
    <base-footer />
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue';
import HomePage from './pages/HomePage.vue';
import BaseFooter from './components/BaseFooter.vue';
export default {
  name: 'app',
  components: {
    HomePage,
    BaseHeader,
    BaseFooter,
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
html {
  margin: 0;
  padding: 0;
}
body {
  margin: 0;
  padding: 0;
}
</style>
