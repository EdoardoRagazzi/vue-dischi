<template>
  <div class="row">
    <div class="col-6 col-md-4 col-lg-3">Prova</div>
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
      axios.get(this.apiURL).then((res) => {
        // console.log(res.data);
        this.listCharacter = res.data;
        console.log(this.listCharacter);
      });
    },
  },
};
</script>

<style>
</style>