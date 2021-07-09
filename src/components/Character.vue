<template>
  <div class="cardi">
    <img :src="details.poster" class="card-img-top" />

    <p>
      {{ details.title }} <br />
      {{ details.author }} <br />
      {{ details.year }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Character",
  props: ["details"],
};
</script>

<style scoped lang="scss">
.cardi {
  padding: 15px;
  text-align: center;
  max-height: 270px;
  width: 200px;
  color: white;
  border: 2px solid black;
  background-color: #2e3a46;
  border-radius: 20px;
  img {
    margin: auto;
    height: 150px;
    width: 150px;
  }
}
</style>




 