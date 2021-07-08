<template>
  <header class="text-center p-5 text-white">
    <h1>{{ message }}</h1>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["message"],
};
</script>

<style>
</style>