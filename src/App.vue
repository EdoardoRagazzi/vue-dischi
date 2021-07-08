<template>
  <div id="app">
    <Header message="Dischi" />
    <ListCharacter />
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
