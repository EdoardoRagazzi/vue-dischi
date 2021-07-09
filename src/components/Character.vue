<template>
  <div class="card p-5 bg-secondary" style="width: 18rem">
    <img :src="details.poster" class="card-img-top" alt="details.title" />
    <div class="card-body g-5">
      <h5 class="card-title">
        <i class="fab fa-accessible-icon"></i>{{ details.title }}
      </h5>
      <p class="card-text"></p>
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item bg-secondary">{{ details.author }}</li>
      <li class="list-group-item bg-secondary">{{ details.year }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Character",
  props: ["details"],
};
</script>

<style>
.list-group {
  flex-direction: initial;
}
.card {
  height: 500px;
}
</style>

 