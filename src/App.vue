<template>
  <div id="app">
    <Nav />
    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>
<script>
import Nav from "./components/Nav";
import Landing from "./views/Landing";
export default {
  components: {
    Nav,
    Landing
  }
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
}
body {
  line-height: 1.6;
}
</style>
