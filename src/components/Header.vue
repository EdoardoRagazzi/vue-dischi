<template>
  <header class="text-center text-white text-uppercase d-block">
    <img src="@/assets/logo.png" alt="" />
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
  img {
    height: 80px;
    float: left;
    padding: 10px;
  }
}
</style>