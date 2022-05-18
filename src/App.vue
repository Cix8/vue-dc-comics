<template>
  <div id="app">
    <AppHeader />
    <main>
      <SeriesList />
      <ShopNav />
    </main>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import ShopNav from "./components/ShopNav.vue";
import SeriesList from "./components/SeriesList.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    SeriesList,
    ShopNav,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";

#app {
  background-color: #1c1c1c;
  padding: 30px 0;

  main {
    color: #ffffff;
  }
}
</style>
