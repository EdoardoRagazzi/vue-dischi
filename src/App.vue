<template>
  <div id="app">
    <Header />
    <div class="d-flex justify-content-center">
      <ListCharacter />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import ListCharacter from "@/components/ListCharacter.vue";

export default {
  name: "App",
  components: {
    Header,
    ListCharacter,
  },
};
</script>

<style lang="scss">
@import "@/style/general.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
