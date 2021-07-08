<template>
  <div class="row">
    <div
      v-for="(item, index) in listCharacter"
      :key="index"
      class="col-6 col-md-4 col-lg-3"
    >
      <div class="card" style="width: 18rem">
        <img src="@/poster" class="card-img-top" alt="..." />
        <div class="card-body">
          <h5 class="card-title">{{ item.title }}</h5>
          <p class="card-text">
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">An item</li>
          <li class="list-group-item">A second item</li>
          <li class="list-group-item">A third item</li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link">Card link</a>
          <a href="#" class="card-link">Another link</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import "axios";
import axios from "axios";

export default {
  name: "ListCharacter",
  data() {
    return {
      apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
      listCharacter: [],
    };
  },
  created() {
    this.getCharacters();
  },
  methods: {
    getCharacters() {
      axios
        .get(this.apiURL)
        .then((res) => {
          // Creo un array di oggetti che è uguale all'array dell'API che mi sono andato a collegare
          // console.log(res.data);
          this.listCharacter = res.data.response;
          console.log(this.listCharacter);
        })
        .catch((error) => {
          console.log("Errore:", error);
        });
    },
  },
};
</script>

<style>
</style>