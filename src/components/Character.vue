<template>
  <div class="card p-5" style="width: 18rem">
    <img :src="details.poster" class="card-img-top" alt="details.title" />
    <div class="card-body g-5">
      <h5 class="card-title">{{ details.title }}</h5>
      <p class="card-text"></p>
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item">{{ details.author }}</li>
      <li class="list-group-item">{{ details.genre }}</li>
      <li class="list-group-item">{{ details.year }}</li>
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
</style>

   "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
            "title": "New Jersey",
            "author": "Bon Jovi",
            "genre": "Rock",
            "year": "1988"