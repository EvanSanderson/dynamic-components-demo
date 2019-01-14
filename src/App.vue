<script>
import TwoColumnPage from "./components/TwoColumnPage";
import ourData from "./data/ourData.json";

export default {
  name: "app",
  components: {
    TwoColumnPage
  },
  data() {
    return {
      pageConfig: []
    };
  },
  created() {
    this.pageConfig = ourData.page_one;
  }
};
</script>

<template>
  <div id="app">
	<h1>Our Page</h1>
	<component :is="pageConfig.type" :slots="pageConfig.slots" />
  </div>
</template>

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
