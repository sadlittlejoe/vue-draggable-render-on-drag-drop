<template>
  <div id="app">
    <ListSharing/>
  </div>
</template>

<script>
import ListSharing from "./components/ListSharing";

export default {
  name: "App",
  components: {
    ListSharing
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
