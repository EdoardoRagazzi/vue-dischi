<template>
  <header class="text-center text-white text-uppercase d-block">
    <div class="logo"><i class="fab fa-spotify fa-4x"></i></div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["message"],
};
</script>


<style scoped lang="scss" >
header {
  background-color: #2e3a46;
  height: 90px;
  margin-bottom: 50px;
  .logo {
    float: left;
    padding: 10px;
    color: green;
    i {
      font-size: 3em;
      color: green;
    }
  }
}
</style>