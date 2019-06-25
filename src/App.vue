<template>
  <div id="app">
    <Greeting/>
    <Calculator/>
  </div>
</template>

<script>
import Greeting from "./components/Greeting.vue";
import Calculator from "./components/Calculator.vue";

export default {
  name: "app",
  components: {
    Greeting,
    Calculator
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
